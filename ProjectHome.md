# Description #
NOAA publishes weather data in a proprietary format, referred to as ISH.  This format is encoded, and they provide a very basic parser ([ishJava](ftp://ftp.ncdc.noaa.gov/pub/data/noaa)) to extract this data if needed.

This project simply takes their existing ishJava parser, and extends it.

# Usage #
In general...
  1. Compile source file
  1. Run from command line, specifying input file (ISH format) and output file

Example...
```
javac noaa/ISHParser.java
java -classpath . noaa.ISHParser 999999_99999_2012 999999_99999_2012.txt
```

# Goal #
Goals of this project:
  * Allow both metric and imperial measurements in output
  * Output in TSV format, rather than fixed length, which allows for simpler import into a DB
  * Allows for more meaningful headers

# Outstanding #
  * Lots of code duplication, clean it up.
  * Make imperial/metric flag available via command line


# References #
  * ISH data lives here - [ftp://ftp.ncdc.noaa.gov/pub/data/noaa](ftp://ftp.ncdc.noaa.gov/pub/data/noaa)
  * Original ishJava parser source lives here - [ftp://ftp.ncdc.noaa.gov/pub/data/noaa/ishJava.java](ftp://ftp.ncdc.noaa.gov/pub/data/noaa/ishJava.java)