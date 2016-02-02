# Exercise 1

###Questions within instructions
We were asked to look at [this website](http://www.recoveredhistories.org) and state what makes us think it is or it is not a trustworthy site for historical texts. I don't think I can answer that as I tend to use journals and conference papers when having to reference a trustworthy source, not web-sites. I have also not had a chance, at this point in time, to look through the material provided by the site, and can therefore not give a fair argument for or against the resource.

### Exercise
We were asked to search for Negro Slavery by Zachari Macaulay, which can be found [here](http://www.recoveredhistories.org/pamphlet1.php?catid=805). This seems a bit long for a pamphlet.

The XML file has been completed and is included in this repository.

### More transformations
Questions were asked at the end of the exercise. Here are the answers:

- What tags would it be looking for in the xml file? 
	- publication_information
		- newspaper_title
		- newspaper_city
		- newspaper_province
		- newspaper_country
		- year
		- month
		- day
		- section_name
	- articletype
	- p
		- mention
			- attribute: keyword
			- attribute: name
			- if there is a country attribute
				- select the city attribute
		- dateline
			- attribute: city
			- attribute:country
			- attribute province
	- transcription_information
		- collection_date
		- transcription_date
		- type
		- repository
		- url
		- method
		- transcriber
  

- What might it do to your markup? 
	- XSL files format the output
	- xsl:value-of get the value of the mentioned element
	- normalize-space removes extra spacing
	- translate replaces parts of a string
	- This xsl will do the following




>for each article

>it will append the id to the word ID

>it will print the publication information listed above

>for each paragraph -> it will remove commas

> it will list the transcription details

> for each name attribute -> replace the commas with underscores and list it, followed by a ";" if it's not the last element.

> for each keyword attribute -> list it and add a ";" if it's not the last element 

> for each country attribute -> if the country is not empty, list the city, province and country in the following format: city_province_country and add a ";" if it's not the last element


- What line would you change in your XML file to get it to point to this stylesheet? 
	- The href of the following line would need to change to point to the new stylesheet

> <?xml-stylesheet type="text/xsl" href="Transcriptions.xsl"?>

