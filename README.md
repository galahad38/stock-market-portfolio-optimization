# Stock Market Portfolio Optimization

## What it does:
It performs Exploratory Data Analysis on desired stocks, plots Trend Lines, Distribution plots, Pair plot, Cumulative Returns plot.
You can use these plots to determine the two most lucrative stocks you would like to add to your portfolio.
Then the code provides you with the optimal weights for the chosen stocks in order to get the highest returns for the lowest risk.

This project was built as part of the academic requirement of the PGP-DSE program at Great Learning Hyderabad.
There is a [Canva Presentation](https://www.canva.com/design/DAFxsZ8-4sI/fPhuHQPefUDUDcopfJGcIg/edit) associated with this project. Please feel free to take a look at it!

Sometimes GitHub is unable to Preview Code Blocks for Jupyter Notebooks. If this happens, you can just view my [Notebook](https://nbviewer.org/github/galahad38/stock-market-portfolio-optimization/blob/main/stock-market-portfolio-optimization.ipynb).

## How to build it yourself:

1. Install [Python](https://www.python.org/downloads/):
2. Install non-standard Python libraries:
     launch command prompt and run this command:
     ```console
     C:\Windows\system32\ pip install ipykernal, jupyterlab, notebook, numpy, pandas, matplotlib, seaborn, yfinance
     ```
3. Download the [Jupyter Notebook](https://github.com/galahad38/book-century-identifier/blob/main/building-the-naive-bayes-model.ipynb).
4. Launch Jupyter Notebook from the Start Menu, and navigate to the folder containing the dataset and Jupyter Notebook you just downloaded.
5. Change the stock tickers and start and end dates in Section 2 as per your choice.
6. Go to Cell -> Run All.
7. Profit!

## How to interpret it:

1) The Line Plots in Section 3.2 give you an idea of how the stock price has changed over the chosen time period. We want our stocks to increase in price over time.
2) The Distribution Plots in Section 3.9 give you an idea of the risk associated with each stock. We want our stocks to have low risk.
3) The Pair Plot in Section 3.11 gives you an idea of which stocks have risks associated with them that are highly correlated. We want our stocks to have some correlation, in that they all grow with the time, but we don't want them to have too high of a correlation, meaning if one stock performs poorly, so does the other.
4) The Cumulative Returns Plot in Section 3.12 gives you an idea of the returns a stock would net you if you'd invested $1 in it at the beginning of the chosen time period. We want our stocks to give us high returns. I don't think I needed to tell you that.
5) Finally, the Markowitz Curve, and subsequent cells will tell you the optimal weights of the two most lucrative stocks obtained in the previous step, that will provide us with the highest returns for the lowest risk.

## My instance and the insights derived:

### Data Collection:
Sourced stock price data for Tesla, Boeing, and Apple for a 5-year period using the Yahoo Finance API, creating a diverse portfolio using stocks from the Automotive, Travel and Consumer Tech industries.

### Data Cleaning:
Dropped irrelevant columns and retained only 'Close' Price.

### Feature Engineering:
Calculated the Daily Returns of each stock.

### Data Visualization: Used Seaborn to visualize price change, price variance, correlation in price change, and daily returns, providing a clear comparison of Apple and Tesla's performance.

![Line Plots](https://github.com/galahad38/stock-market-portfolio-optimization/assets/19240929/f9d057d0-689a-406a-b16b-170d583f4afd)

We're able to see the impact of real-world events on the stock price of a company:
* Tesla's stock price skyrockets in correlation to its phenomenal sales track record.
* Boeing's stock price plummets in correlation to the Restrictions placed on Air-Travel due to the COVID-19 pandemic. 

![Distribution Plots](https://github.com/galahad38/stock-market-portfolio-optimization/assets/19240929/2bdd34f4-412b-4a3b-abce-def2a86e849e)

The stock with the widest distribution curve is the one with the highest variance, and thus, the highest risk associated with it. In this case, surprisingly, it's Apple.

![Pair Plot](https://github.com/galahad38/stock-market-portfolio-optimization/assets/19240929/4f9b766c-6e26-4e10-8adc-ed8b74435c49

We can see that:
* the Daily Returns of Apple and Boeing are highly correlated.
* the Daily Returns of Boeing and Tesla are not nearly as highly correlated.
* the Daily Returns of Apple and Tesla are moderately correlated, and the value lies in between the other two.

![Cumulative Returns Plot](https://github.com/galahad38/stock-market-portfolio-optimization/assets/19240929/31ebd410-a1c6-4cf6-bc44-fb87cc8db081)

If you'd invested $1 at the start of the chosen 5-year time period:
* Tesla would've returned more than $12
* Apple would've returned more than $1.5 (I believe there may have been a stock split at some point)
* Boeing would've returned around 80 cents. 
We shall proceed with Tesla and Apple in our portfolio, and try to calculate how much of our total capital should be invested in each stock in our two-stock portfolio.

![Markowitz Curve](https://github.com/galahad38/stock-market-portfolio-optimization/assets/19240929/a256e9fe-73a1-4939-aaf2-c21f7667b4ac)

We can see that at a certain point, with increase in risk, there is an increase in returns. This is known as the Efficient Frontier.
However we can see that if we were to proceed in the opposite direction, with increase in risk, there is a decrease in returns. This is known as the Inefficient Frontier. No one would want to invest in portfolios associated with this frontier.
We can see our optimal portfolio at the minima of the parabola, providing the highest returns for the lowest risk.
In our case, this point is associated with a portfolio with 115% of the capital invested in Apple and -15% of the capital invested in Tesla. This doesn't make a whole lot of sense. How can you have -15% of your capital invested in a stock? The answer is simple - The curve is letting us know that the optimal portfolio would have us shorting Tesla for 15% of our capital, then investing this extra 15% along with our existing 100% capital into Apple.

### Future Scope:
I am satisfied with the outcome of this project. However it is simplistic and undoubtedly a prototype with huge scope for improvement:
1) I can use plotly to plot better plots, in higher dimensions, to better understand the price behaviour of the stocks.
2) This project is limited to calculating the optimal weights of a two-stock portfolio. I can implement Machine Learning to overcome this.

**However I will likely not pursue these objectives any time soon, so feel free to contribute to this Project!**
