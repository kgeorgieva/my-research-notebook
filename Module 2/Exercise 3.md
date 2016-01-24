# Running the canadiana script

This exercise consisted of us installing a bunch of software in order to run the canadiana script.

The windows instructions were clear. There is an easier way to get to the environment variables to change them: just open start, search 'environment' and then click on 'edit system environment variables'.

Also note that if you download the wget exe for 64 bit you need to add it to the c:/Windows folder (as mentioned) and rename it to just wget instead of wget64. Alternatively add it to the system environment variables.

The total number of records retrieved through the exercise's example is 56,845, slightly higher than it was when the exercise was set up.

The provided sed and split command does not seem to work in windows. It just ends up creating thousands of files some with just brackets in them.

Sed command uses regex like expressions to find and, in this case, replace a particular string. In the exercise the sed command is as using the following expression:

> s/oocihm/\n&/2g

This seems to mean substitute 'oocihm' with the secod bit of the line containing it and a new line. 

### Fixing the split
In order to fix the split one needs to first understand the command and its options. [This](https://www.gnu.org/software/coreutils/manual/html_node/split-invocation.html) is a nice resource for that.

Strange,
>split --help

seems to have a lot more limited parameter options. Is this because of it being the windows version? I can't seems to be able to use a separator to split the files, and each JSON object has a different length, so line numbers won't help. 

[This](http://www.theunixschool.com/2012/06/awk-10-examples-to-split-file-into.html) is a good resource for the alternative I've decided to use, gawk.

None of these tools seem to be working or I am not understanding them.

I have written an application to do the splitting for me, too much fighting with bad windows behaviour. I will push this jar along with the exercise so it can be used by others.

I can't answer the sed question from this exercise due to having to use an alternative solution for the splitting. I can speak generally about the use of regex to retrieve patterns one is looking for.

Regular expressions, which sed can use to substitute and find patterns, allow a user to filter through data in order to grab a piece that they need. They are also very useful when validating inputs, such as e-mail addresses having to contain @ and .xx. 


