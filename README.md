# SABR Calibration

European options are often priced and hedged using Black’s model. Option prices are quoted by stating the implied volatility. In practice, options with different strikes require different volatilities to match market prices. 

Handling these market skews and smiles correctly is important to fixed income desks. Local volatility models have been used to manage these skews and smiles. Although local volatility models are self-consistent, arbitrage-free and can be calibrated to match observed market skews and smiles, it has been observed that the dynamic behaviour of smiles and skews predicted by local volatility models contradicts the one observed in the marketplace. 

A stochastic volatility model, called the SABR model, is derived to solve this problem. The SABR model is a parameterized pricing model for European options. To use the model properly, it must be calibrated to market skews and smiles. 

Vanilla European options are priced and hedged using Black-Scholes or Black model. Under the assumption of a log-normal model, there is a one-to-one corresponding between the price of the option and the volatility parameter σB. Therefore, option prices are often quoted by stating the so-called implied volatility in the marketplace. 

In reality, options with different strikes require different volatilities to match their market prices. This is the market skew and smile. Usually, with respect to the strike, the word skew is for the slope of volatility and smile is for its curvature. The inherent contradiction of using different volatilities for different strikes in Black’s model makes it difficult to rigorously handle skew/smile risks.

The development of local volatility models and stochastic volatility approaches has been a major advance in managing market skews and smiles. Although local volatility models are self-consistent, arbitrage-free and can be calibrated to match observed market skews and smiles, it is observed that the dynamic behaviour of smiles and skews predicted by local volatility models contradicts the one observed in the marketplace. This means that it is not proper to use a Markovian model based on a single Brownian driving force to handle market skew/smile risks. 

Among those stochastic volatility models, the SABR model is the simplest stochastic volatility model which is homogenous in underlying rates and volatilities. The SABR model can be used to accurately fit the implied volatility curves observed in the market for any single tenor and correctly predict the dynamics of the implied volatility curves, which thus yields correct and stable hedges. Moreover, this model allows the market price and the market risks to be obtained immediately from Black’s formula.

Consider a European option whose matured payoff at a maturity of T, denoted by VT , depends on a underlying rate FT . Under the appropriate martingale measure, a SABR model of the underlying rate process F is assumed to be. Clearly, it is an arbitrage-free model. Under the model, F follows a stochastic CEV process. Particularly, if β = 0, 0.5, 1, then it corresponds to a stochastic normal, CIR and log-normal processes, respectively. 

The volatility term follows a geometric Brownian motion where the parameter ν is the volatility of the stochastic volatility term. In the model, F is in a general setting. In various cases, it can an equity index, a currency exchange rate, a forward interest swap rate, or an interest futures/forward rate. For interest rate derivatives, a forward risk-neutral measure is chosen such the underlying rate is a martingale.

Clearly, those parameters in the SABR model are not market observable. Therefore, calibration procedure is the key step so that the calibrated SABR model captures the market skews and smiles. In our fixed income derivative applications, we need to consider swaptions, caplets/floorlets, and caps/floors. Swaptions, caplets and floorlets are examples of a single European option. Caps/floors are a portfolio of caplets/floorlets. In all our applications, the parameter β is selected exogenously.

For applications to swaptions, the model is used to fit the swaption market skews/smiles. While for applications to caps/floors, it can be applied to fit the cap/floor market skews/smiles. It should be noticed that there is no standard approach for model calibrations. However, the basic principle is to fit market liquid products as well as possible. In the following, there are two calibration approaches, one for the swaption market and the other one for the cap/floor market.


Clearly, those parameters in the SABR model are not market observable. Therefore, calibration procedure is the key step so that the calibrated SABR model captures the market skews and smiles. In our fixed income derivative applications, we need to consider swaptions, caplets/floorlets, and caps/floors. Swaptions, caplets and floorlets are examples of a single European option. 

Caps/floors are a portfolio of caplets/floorlets. In all our applications, the parameter β is selected exogenously. For applications to swaptions, the model is used to fit the swaption market skews/smiles. While for applications to caps/floors, it can be applied to fit the cap/floor market skews/smiles. It should be noticed that there is no standard approach for model calibrations. However, the basic principle is to fit market liquid products as well as possible. In the following, there are two calibration approaches, one for the swaption market and the other one for the cap/floor market.

The calibration to the cap market is more involved. Each cap is a portfolio of a sequence of caplets. The SABR model is applied to each individual caplet. Although, as mentioned before, the parameter β is still selected exogenously, we have to consider term structures of α, ρ and ν, respectively. The cap market provides market values of caps of terms from 1-year to 20-year with quarterly settlements. 

The SABR becomes the calibrated cap pricing model which can handle cap market skews and smiles. This is the calibration approach for the cap market. It should be noticed that there is no presumption that this is the best approach to calibration to the cap market. However, under this practically feasible and aggressively simplified approach, matching of the at-the-money caps is given higher priority over the calibration to the skews and smiles. This is also recommended by the cap market due to the higher liquidity of the at-the-money caps.



Reference:

https://finpricing.com/lib/EqSpread.html

https://zenodo.org/record/6625994#.YqEOK6gpBD8

https://zenodo.org/record/6625994/files/sabrCalibration.pdf
