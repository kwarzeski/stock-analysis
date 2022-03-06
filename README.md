# VBA of Wall  Street

## Overview of Project
This project is to create a macro to analyze stock data. The data given is for specific stocks in 2017 and 2018, but the code is written to be usable for future years. The initial code implementation was slow and the code was refactored for speed, since future data could include thousands more rows of data.

## Results
 The stocks chosen did well in 2017 and poorly in 2018. ENPH is the only stock that did well both years. TERP is the only stock that did poorly both years.
 
 The code for 2017 initially ran in 1.38 seconds - the refactored code ran in 0.23 seconds. Similarly, the code for 2018 initially ran in 1.15 seconds - the refactored code ran in 0.26 seconds. The refactored code was a significant improvement and would be even more noticeable as the dataset grew.
 
## Summary
By refactoring the code, it now runs faster. The code only loops through the rows of data once, instead of once per ticker (eleven times in this case). As the data grows this could be a significant change. A disadvantage is that time was taken to rewrite the code.

The original script may have slowed down as more data was added and would have been a poor user experience.

The code assumes that the data is sorted by ticker, then by date. By adding a line that sorts the data before interating through it, we can prevent errors if the code is unsorted.

Additionally, the code assumes a set of tickers. We could build the list of tickers as we loop through the rows of data, so that if new tickers are added, then are included.
