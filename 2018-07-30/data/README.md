Description of the files in the folder.
- Each file is named based on `{id}.csv.bz2` convention where `{id}` is the id of the stock in iran's market (based on website [TSETMC][1]). For example if you go to the url `http://www.tsetmc.com/loader.aspx?ParTree=151311&i={id}` where `{id}` is the same id in the file name, you will find the page of the stock in _TSETMC_. for example
`2589887561569709.csv.bz2` => `http://www.tsetmc.com/loader.aspx?ParTree=151311&i=2589887561569709`
- Each file (after extracting it to `{id}.csv`) contains is like:
```
Date,High,Low,Final,Close,Open,Yesterday,Value,Volume,Count
2018-02-21,779.0,745.0,776.0,779.0,745.0,742.0,50334044074.0,64877868,2956
2018-02-19,766.0,735.0,742.0,740.0,766.0,765.0,13120688184.0,17684084,1171
2018-02-18,780.0,750.0,765.0,760.0,760.0,773.0,17450282940.0,22796337,1245
```
This is common [CSV (Comma-Separated Values)][2] format. Data is aggregated by _Day_ resolution (I assume that you should know what this means!).
Each column's meaning is as follow:
    - __Date__: Gregorian Date
    - __High__: Highest traded price
    - __Low__: Lowest traded price
    - __Final__: Final price of the day (some weighted average of prices through day)
    - __Close__: Last traded price
    - __Open__: First traded price
    - __Yesterday__: Yesterday's Final price
    - __Value__: Sum of the `price*volume` of all transactions
    - __Volume__: Sum of all volumes of transactions
    - __Count__: Number of transactions in that day


[1]: http://www.tsetmc.com/Loader.aspx?ParTree=15131F
[2]: https://en.wikipedia.org/wiki/Comma-separated_values