In the first part of the exercise we had to add "~" to the beginning of every line containing the word "to" as follows:

> (.+\<to\>)
> replaced with ~\1

The recommended regular expression 
> \r\n[^~].+

does not take into account lines that were separated by a new line halfway. Such as:

>Eddy and Moss to the collector of the customs at New Orleans, April 23, 

>1843 321 

To solve I tried an expression that checks the following:

- the previous line starts with "~"
- the length of the previous line is exactly 79

The above experiment resulted in the following regular expression that finds the warped lines
> (\r\n[~](.){63,80})((\r\n)+)([^~](.){1,55}\d $)(\r\n)

This expression does the following:

- \r\n matches a new line
- [~] matches a ~ (we only care to fix the ones we'll keep)
- (.){65,80} matches any characters. The string requiring a minimum of 65 and maximum of 80 characters
- (\r\n)+ matches any amount of new lines
- [^~] matches a line not having a ~
- (.){1,55} matches any characters, where the string can have a minimum length of 1 and maximum length of 50
- \d $ matches ending with a digit and a space
- \r\n matches the new line after

I then replaced with the following:

>\1\5\7

The sections look a bit strange because of the inner brackets of the query.  Sections 1, 5 and 7 refer to:

- section 1 -> (\r\n\[~](.){65,80})
- section 5 -> (\[^~](.){1,55}\d $)
- section 7 -> (\r\n)

This replace will remove the newline added by the warping, adding the missing information to its appropriate line.

The next step in the exercise is to remove the lines we will not be using, in other words the lines without "~" at the start. To do this the provided regular expression was used:

> \r\n[^~].+

The next step is to replace the new lines with nothing. On my Windows machine new lines are found as follows:

> \r\n

which means carriage return and new line.

Textwrangler uses "^\r" which means begining of a line with a carriage return.

Replacing all the new lines in the file will result in no separation between the various lines. I'll replace the new lines to have each letter on a line as follows:

> replacing (\r\n)+

> with \r\n

### Transforming to CSV
First we need to remove the page numbers as follows:

> match (,)( [0-9]{4})(.+)

> replace with \2

Then we need to replace the "~" we added by doing the following:

> replace \r\n[~]

> with \r\n

The reason for checking for the new line is to make sure we don't remove a "~" inside the descriptions.

Next we replace the word "to" with a comma by matching:

> ( to\>)

Then we had to manually replace data that had extra commas, which we can find using:

> .+,.+,.+,

There were also some strange dates such as 184Q which were not picked up correctly by the exercise removing pages, so the pages for these lines had to be removed manually.

We then add the headers

>Sender, Recipient, Date

The above cleaning process seems to have worked well. Only one of the lines sees to have been missed for some reason and it was removed manually.




