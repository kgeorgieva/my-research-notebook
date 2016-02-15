# Exercise 4 - Named entity recognition

This exercise is about named entity recognition, which uses machine learning and statistical models as a technique to find data.

We had to download [Standford NER](http://nlp.stanford.edu/software/CRF-NER.shtml#Download) and start off by using the GUI. First I had to update my Java version to Java 8 (it was about time anyway. Lambdas finally!)

In the GUI we used the "Location, Person, Organisation" classifier and saw the words appear colour coded accordingly once we processed the data.

The next step was to output this to a file. For some reason, the GUI's export does not seem to enable the exporting of the tagged data even though the option is there.

To do the export the following command was given to us:

> java -mx500m -cp stanford-ner.jar edu.stanford.nlp.ie.crf.CRFClassifier -loadClassifier classifiers/english.all.3class.distsim.crf.ser.gz -textFile texas-letters.txt -outputFormat inlineXML > “my-ner-output.txt”

The above command, however, gave me an [NoClassDefFoundError](https://www.google.co.za/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&ved=0ahUKEwjRqMH-u_rKAhXIlB4KHV4vCbAQFggaMAA&url=https%3A%2F%2Fdocs.oracle.com%2Fjavase%2F7%2Fdocs%2Fapi%2Fjava%2Flang%2FNoClassDefFoundError.html&usg=AFQjCNGXxHLucM58MwiDLuk7_q2IQhLicA&sig2=kt5F2Zzfyi_5aOpDgeMijg&bvm=bv.114195076,d.dmo&cad=rja) for the slf4j logger. This means that the application cannot find that dependency. The dependencies in this application are placed in the "lib" folder, therefore, in order for the application to pick these up, we can add the lib folder to our command:

> java -mx1000m -cp stanford-ner.jar;lib/* edu.stanford.nlp.ie.crf.CRFClassifier -loadClassifier classifiers\english.all.3class.distsim.crf.ser.gz -textFile letters.txt  -outputFormat inlineXML > my-ner-output.txt

The above command has changed by adding the ";lib/* " part and by removing the quotation marks from the output text file name.

The resulting tagged file has been included as NER-output.txt.