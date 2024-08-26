# structural_credit

A structural credit model is a type of credit risk model that assesses the likelihood of a company defaulting on its debt obligations based on the structure of its balance sheet, particularly the relationship between its asset value and its debt. The most well-known structural model is the Merton model, but the concepts can be extended to more complex frameworks.


Asset Value Dynamics:
The company's assets are assumed to follow a geometric Brownian motion. This stochastic process describes how the value of the company's assets evolves over time. The equation is:
dV = V * (mu * dt + sigma * dW)
Where:
V is the current value of the company's assets.
mu is the drift rate (expected return on assets).
sigma is the volatility of the asset value.
dt is a small time increment.
dW is a Wiener process (Brownian motion increment).

Distance to Default:
The distance to default measures how far the company's asset value is from the default point (typically the face value of its debt) in terms of standard deviations. The formula is:
Distance to Default = (log(V / D) + (r + 0.5 * sigma^2) * T) / (sigma * sqrt(T))
Where:
V is the current value of the company's assets.
D is the face value of the company's debt.
r is the risk-free interest rate.
sigma is the volatility of the asset value.
T is the time to maturity of the debt.

Default Probability:
The default probability is the probability that the company's asset value will fall below the default point by the time the debt matures. This is computed using the cumulative distribution function (CDF) of the standard normal distribution:
Default Probability = N(-Distance to Default)
Where:
N() is the cumulative distribution function of the standard normal distribution.
Distance to Default is as calculated above.

Credit Spread:
The credit spread is the additional yield over the risk-free rate that compensates investors for the risk of default. It can be estimated as:
Credit Spread = Default Probability * (1 - Recovery Rate)
Where:
Default Probability is the probability that the company will default.
Recovery Rate is the proportion of the bond's value that is expected to be recovered in the event of default.



Asset Value Dynamics:
dV = V * (mu * dt + sigma * dW

Distance to Default:
Distance to Default = (log(V / D) + (r + 0.5 * sigma^2) * T) / (sigma * sqrt(T))

Default Probability:
Default Probability = N(-Distance to Default)

Credit Spread:
Credit Spread = Default Probability * (1 - Recovery Rate)
