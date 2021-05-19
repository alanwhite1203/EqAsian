# Equity Asian Option 

An Asian option or average option is a special type of option contract  where the payoff depends on the average price of the underlying asset over a certain period of time. The payoff is different from the case of a European option or American option, where the payoff of the option contract depends on the price of the underlying stock at exercise date. 

 Asian options allow the buyer to purchase or sell the underlying asset at the average price instead of the spot price. Asian options are commonly seen options over the OTC markets. Average price options are less expensive than regular options and are arguably more appropriate than regular options for meeting some of the needs of corporate treasurers. Average can be calculated in a number of ways (daily, weekly, monthly, etc.). This presentation provides an overview of Asian equity option product and valuation. 

One advantage of Asian options is that they reduce the risk of market manipulation of the underlying instrument at maturity. Another advantage of Asian options involves the relative cost of Asian options compared to European or American options. Because of the averaging feature, Asian options reduce the volatility inherent in the option; therefore, Asian options are typically cheaper than European or American options.

Asian options have relatively low volatility due to the averaging mechanism. They are used by traders who are exposed to the underlying asset over a period of time. The Asian option can be used for hedging and trading Equity Linked Notes issuance. The arithmetic average price options are generally used to smooth out the impact from high volatility periods or prevent price manipulation near the maturity date, which makes the options less expensive.

	Asian Option Introduction

	An Asian option or average option is a special type of option contract  where the payoff depends on the average price of the underlying asset over a certain period of time 
	The payoff is different from the case of a European option or American option, where the payoff of the option contract depends on the price of the underlying stcok at exercise date.
	Asian options allow the buyer to purchase (or sell) the underlying asset at the average price instead of the spot price.
	Asian options are commonly seen options over the OTC markets.
	Average price options are less expensive than regular options and are arguably more appropriate than regular options for meeting some of the needs of corporate treasurers.
	average can be calculated in a number of ways (daily, weekly, monthly, etc.).

	The Use of Asian Options

	One advantage of Asian options is that they reduce the risk of market manipulation of the underlying instrument at maturity. 
	Another advantage of Asian options involves the relative cost of Asian options compared to European or American options. Because of the averaging feature, Asian options reduce the volatility inherent in the option; therefore, Asian options are typically cheaper than European or American options.
	Asian options have relatively low volatility due to the averaging mechanism. They are used by traders who are exposed to the underlying asset over a period of time
	The Asian option can be used for hedging and trading Equity Linked Notes issuance.
	The arithmetic average price options are generally used to smooth out the impact from high volatility periods or prevent price manipulation near the maturity date, which makes the options less expensive.

	Valuation

	The payoff of an average price call is max(0, Savg - K) and that of an average price put is max(0, K- Savg), where Savg  is the average value of the underlying asset calculated over a predetermined averaging period. 
	If the underlying asset price, S, is assumed to be lognormally distributed and Save is a geometric average of the S’s, analytic formulas are available for valuing European average price options. This is because the geometric average of a set of lognormally distributed variables is also lognormal. 
	When, as is nearly always the case, Asian options are defined in terms of arithmetic averages, exact analytic pricing formulas are not available. This is because the distribution of the arithmetic average of a set of lognormal distributions does not have analytically tractable properties.
	However, the distribution of arithmetic average can be approximated to be lognormal by moment matching technical, which leads to a good analytic approximation for valuing average price options. 
	One calculates the first two moments of the probability distribution of the arithmetic average in a risk-neutral world exactly and then fit a lognormal distribution to the moments.
	Consider a newly issued Asian option that provides a payoff at time T based on the arithmetic average between time zero and time T. The first moment, M1 and the second moment, M2, of the average in a risk-neutral world can be shown to be

M_1=(e^(r-q)T-1)/(r-q)T S_0
M_2=(2e^[2(r-q)+e^2 ]T S_0^2)/((r-q+σ^2)(2r-2q+σ^2)T^2 )+(2S_0^2)/((r-q)T^2 ) (1/(2(r-q)+σ^2 )-e^(r-q)T/(r-q+σ^2 ))
where 
r 	the interest rate
q	the devidend yield
q≠r.


	By assuming that the average asset price is lognormal, you can use Black's model to price an Asian option.
	The present value of an Asian call option is given by

〖PV〗_C=(M_1 N(d_1 )-KN(d_2))D
d_1,2=(ln(M_1⁄K)±(σ^2 T)⁄2)/(σ√T)
σ^2=1/T ln⁡(M_2/(M_1^2 ))
where 
D 	the discount factor
N 	the cumulative standard normal distribution function
T	the maturity date

                                                            
	The present value of an Asian put option is given by

〖PV〗_P=(KN(〖-d〗_2 )-F_0 N(-d_1 ))D

	We can modify the analysis to accommodate the situation where the option is not newly issued and some prices used to determine the average have already been observed. 
	Suppose that the averaging period is composed of a period of length T1 over which prices have already been observed and a future period of length T2 (the remaining life of the option). Suppose that the average asset price during the first time period is S. The payoff from an average price call is

max((S ̅T_1+S_avg T_2)/(T_1+T_2 )-K,0)
where 
Savg 	the average asset price of period T2 (future period)
S ̅	the spent average asset price of period T1 (realized period)

This is the same as
T_2/(T_1+T_2 ) max(S_avg-K^*,0)
where
K^*=T_2/(T_1+T_2 ) K-T_1/T_2  S ̅

	When K* > 0, the option can be valued in the same way as a newly issued Asian option provided that we change the strike price from K to K* and multiply the result by t_2/(t_1+t_2) 

〖PV〗_C=T_2/(T_1+T_2 ) (M_1 N(d_1 )-K^* N(d_2))D
〖PV〗_P=T_2/(T_1+T_2 ) (K^* N(〖-d〗_2 )-M_1 N(〖-d〗_1 ))D

	When K* < 0 the option is certain to be exercised and can be valued as a forward contract. The value is

〖PV〗_C=T_2/(T_1+T_2 ) (M_1-K^* )D
〖PV〗_P=T_2/(T_1+T_2 ) (K^*-M_1 )D

	A Real World Example

Face Value	3361.12
Currency	CAD
Start Date	1/10/2017
Maturity Date	7/10/2017
Call or Put	Call
Buy or Sell	Sell
Underlying Assets	.GSPTXBA
Position	-2790.764362
Spent Average	4104.9327




References:

https://finpricing.com/lib/IrCurveIntroduction.html

https://bitbucket.org/cmrm11/eqasian/downloads/EqAsian-2.pdf

