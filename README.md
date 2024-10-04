# Creating & Analyzing Equity Portfolios (with rebalancing)

__Objectives:__

-> Find out if active rebalancing where Weights are restored to initial/target weights at the end of each day will result in upward shift of efficient frontier
-  Doing so will result in selling daily winners and buying daily losers to restore original weights. Contrarian Trading Strategy



__Method:__

1. We import 'scipy.optimize', for python to optimise what we want, be it the maximum return portfolio, or the one with the lowest risk.
   - We use a constraint function, and a function to input what we want to maximize or minimize
   - We create 10,000 portfolios within the constraints given (what we want to do - be it maximise return or find one with lowest Risk or highest RaR) with differing weights and plot them using matplotlib
   - We plot the daily rebalanced portfolio and it's efficient frontier against the one that was not rebalanced to compare performance


__Key Learnings:__

1. To maximise RaR, the optimizer function returned that we should have:
   - 31.3% MSFT, 24.32% TSLA and 22.88% GE, 21.47% AAPL, none of the rest, as these 4 are on the efficient frontier.
   - The CAGR of this portfolio will be 40.75%!
   - The Volitility 27.27% (Standard Deviatoin)
   - Risk Adjsuted Return (RaR) at 1.49! 
<img width="903" alt="image" src="https://github.com/user-attachments/assets/d1807e8d-b1da-47d7-9996-2fe34cdda7f0">


2. Significant Rebalancing Costs eat up Rebalancing Benefits
   - Solution: Reduce Rebalacing Frequency to monthly/quarterly (reduces costs but also benefits)
   - Only rebalance if calculated rebalancing costs are lower than rebalancing benefits
     
3. Upward Shift of Efficient Frontier when balanced daily: (as could be seen with the 2 efficient frontiers!)
- equal risk & more return or
- equal return & less risk

  <img width="920" alt="image" src="https://github.com/user-attachments/assets/5e1b9869-f1e0-4adc-ba16-505accc474cb">


4. As I was optimizing the past here:<br>
- Very unlikely we had selected this optimal portfolio back then (look ahead bias)! <br>
- Very unlikely this will be the optimal portfolio in the future (past performance is not a good indicator for future performance)!
