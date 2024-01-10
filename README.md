# stock-market-portfolio-optimization
1. Performing Basic Exploratory Data Analysis on popular stocks
2. Selecting popular stocks and putting together a basic portfolio
3. Optimizing the weights of each stock in the portfolio using Modern Portfolio Theory
4. Plotting the Markowitz curve for the selected stocks and determining the optimal weights that are expected to give us the highest returns for the lowest risk.
5. Canva Presentation describing the findings: https://www.canva.com/design/DAFxsZ8-4sI/fPhuHQPefUDUDcopfJGcIg/edit
6. You can change the stock tickers and the date range in the code to repeat the project and perform preliminary analysis on basic stock portfolios.

Steps taken:
1) Data Collection: Sourced stock price data for Tesla, Boeing, and Apple for a 5-year period using the Yahoo Finance API.
2) Data Cleaning: Dropped irrelevant columns
3) Feature Engineering: Calculated the Daily Returns of each stock
4) Data Visualization: Used Seaborn to visualize daily returns, providing a clear comparison of Apple and Google's performance.
5) Cumulative Returns Analysis: Calculated the cumulative returns of the considered stocks, and chose the stocks that were more lucrative over the considered 5-year period.
6) Portfolio Optimization: Obtained weights for the considered stocks that would give the best returns for the lowest risk using the Markowitz Curve.
