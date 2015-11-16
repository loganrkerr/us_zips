# TopoJson files of U.S. zip codes by Metropolitan Statistical Area (MSA) number

zip_codes_for_the_us.json is a [TopoJson file of U.S. zip codes assembled by Jeff Friesen](https://gist.github.com/jefffriesen/6892860).

MSA.tsv is modified from a table created by the [Department of Labor Office of Worker's Compensation](https://safelyhome.wordpress.com/2012/08/06/u-s-zip-codes-and-msas-on-a-convenient-table-thank-you-dol-owcp/) which matches zip codes with corresponding MSA numbers. 

Using `topojson`, I added a property for MSA numbers and names to zip_codes_for_the_us.json:
```bash
topojson -o zip_codes_with_msa.json -e MSA.tsv --id-property=zip,zip_code -p name,state,MSA_number,MSA_name -- zip_codes_for_the_us.json
```
