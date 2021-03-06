# Betfair
## Collect odds
To begin collecting odds you must run the `betfair.py` script using the following command:
```
python3 betfair.py appKey sessionToken &
```
### Create Application Key
To create an Application Key visit: <br/> http://docs.developer.betfair.com/docs/display/1smk3cen4v3lu3yomq5qye0ni/Application+Keys#ApplicationKeys-HowtoCreateAnApplicationKey <br/>
### Obtain Session Token 
* Login to betfair.com.
* Go to https://developer.betfair.com/exchange-api/accounts-api-demo/ and copy your session token.

## Clean data
To clean the data (remove noise and anomalous results), run the `cleanData.py` script using the following command:
```
python cleanData.py directory
``` 
where `directory` is the directory that contains the `.csv` files to be cleaned. This will create a new directory `CLEANED_FILES` within `directory` which will contain the cleaned `.csv` files.

## Plot match odds
To plot collected odds for a particular match run the `plotMatchOdds.py` script using the following command:
```
python plotMatchOdds.py example.csv
```
You can produce a more detailed plot which includes shaded regions for when the match is inplay, and dashed lines for goals using the following command:
```
python plotMatchOdds.py example.csv extraMinsFirstHalf extraMinsSecondHalf minOfGoal1 minOfGoal2 ...
```
