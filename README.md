# Alexa_Top_Site_query
Java code adapted from the AWS exemple to manually Grab the Alexa top 200 list with country code as an input


1 - Compile : javac TopSites.java
2 - run it with your AMAZON IAM programmatic keys + the country code : java TopSites xxxxxxxxxxx yyyyyyyyyyyyyy FR
output is a xml file alex.txt

CLI command to extract the domains as a list from the XML file :
grep '<aws:DataUrl>' alex.txt | awk -F">" '{print $2}' | awk -F"<" '{print $1}' >> ats_x.csv
