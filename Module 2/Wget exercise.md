# Getting data via identifiers using Wget

Query to use:
> wget -r -H -nc -np -nH --cut-dirs=2 -A .txt -e robots=off -l1 -i ./items.txt -B 'http://archive.org/download/'

The above query means:

 * get
 * recursively (-r)
 * with a maximum depth of 1 (-l1)
 * while enabling spanning across multiple hosts (-H)
 * while overwriting duplicates (-nc) 
 * keeping it only records within this archove(-np)
 * without adding the host as the prefix to directory names (-nH)
 * keeping the hierarchy flat (--cut-dirs)
 * downloading the text files (those ending in .txt) (-A .txt)
 * and setting the robots option to off (-e robots=off)
 * avoiding visibility of passwords (-i) -> i feel this was not relevant to the current request as no authentication was necessary.
 * using file items.txt
 * using the provided URL as the point of reference for the items in the file (-B 'http://archive.org/download/')

The items.txt and a few resulting file samples have been uploaded with this exercise.