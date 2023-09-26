#Inspiration from UTOR Bootcamp Ressources & Activity + ChatGPT
#MICK CHARBONNEAU
#9/25/23

CHAT GPT

# create a if loop to see if it worked if not return an error code
        if response.status_code == 200:
            data = response.json()
            
            # if it work it will return the btc price
            btc_price_cad = data["data"]["1"]["quotes"]["CAD"]["price"]
            return btc_price_cad
        else:
            print("Failed to fetch BTC price. Status code:", response.status_code)
            return None
    except Exception as e:
        print("An error occurred:", e)
        return None

if response.status_code == 200:
            data = response.json()
            
            # get the current ETH price in CAD
            eth_price_cad = data["data"]["1027"]["quotes"]["CAD"]["price"]
            return eth_price_cad
        else:
            print("Failed to fetch ETH price. Status code:", response.status_code)
            return None
    except Exception as e:
        print("An error occurred:", e)
        return None

plt.figure(figsize=(10, 6))
plt.title("Probability Distribution of Final Portfolio Values (10 Years)")
plt.xlabel("Portfolio Value")
plt.ylabel("Frequency")
plt.hist(final_portfolio_values, bins=30, density=True, alpha=0.7, color='blue', edgecolor='black')

# Calculate the 5% and 95% confidence intervals
ci_lower = np.percentile(final_portfolio_values, 5)
ci_upper = np.percentile(final_portfolio_values, 95)

# Highlight the 5% and 95% confidence intervals
plt.axvline(ci_lower, color='red', linestyle='--', label='95% CI Lower')
plt.axvline(ci_upper, color='green', linestyle='--', label='95% CI Upper')


mean_daily_returns = daily_returns.mean()
cov_matrix = daily_returns.cov()

# Set the number of simulations
num_simulations = 500

# Set the number of trading days in a year
num_trading_days = 252

# Initialize an empty array to hold simulation results
simulation_results = np.zeros((num_simulations, num_trading_days))

# Set the initial portfolio value
initial_portfolio_value = 100000  # Replace with your initial investment amount

# Configure and run the Monte Carlo simulation for 10 years
for s in range(num_simulations):
    portfolio_values = []
    weights = np.random.random(2)
    weights /= np.sum(weights)
    for d in range(num_trading_days):
        daily_return = np.random.multivariate_normal(mean_daily_returns, cov_matrix)
        portfolio_return = np.sum(weights * daily_return)
        portfolio_value = initial_portfolio_value * (1 + portfolio_return)
        portfolio_values.append(portfolio_value)
    simulation_results[s, :] = portfolio_values




for s in range(num_simulations):
    portfolio_values = []
    weights = np.random.random(2)
    weights /= np.sum(weights)
    for d in range(num_trading_days):
        daily_return = np.random.multivariate_normal(mean_daily_returns, cov_matrix)
        portfolio_return = np.sum(weights * daily_return)
        portfolio_value = initial_portfolio_value * (1 + portfolio_return)
        portfolio_values.append(portfolio_value)
    simulation_results[s, :] = portfolio_values

