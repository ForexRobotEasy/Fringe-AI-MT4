# Fringe AI MT4

This is an example code for the Fringe AI MT4 Expert Advisor developed by the Forex Robot Easy Team. For detailed reviews and trading results of the official product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/review-fringe-ai-mt4-advanced-forex-software-for-supply-and-demand-analysis/).

## Product Description

Fringe AI MT4 is an advanced forex trading software that utilizes supply and demand analysis to identify potential trading opportunities. It is designed to work on the MetaTrader 4 platform and supports multiple currency pairs.

The Expert Advisor (EA) uses a custom indicator function to perform the supply and demand analysis and determine the entry zone. It checks if there are any open trades and if the current symbol and timeframe are supported.

The EA calculates the stop loss and take profit levels based on user-defined parameters. It then opens a trade using the OrderSend function with the specified lot size, entry price, stop loss, take profit, and other necessary parameters. If the trade is opened successfully, the trade ticket is printed. Otherwise, an error message is printed with the corresponding error code.

Please note that this code is not an exact copy of the original product. It only provides an approximate description of the necessary parameters for the operation of the product based on the original description. The official trading robot is developed and published on the MQL5 website, and this code serves as an example of how the product can work.

## External Parameters

- **EATitle**: The title of the Expert Advisor (default: 'Fringe AI MT4')
- **LotSize**: The lot size for opening trades (default: 0.01)
- **StopLossPercent**: The percentage of the current Ask price to use for calculating the stop loss level (default: 1.0)
- **TakeProfitPercent**: The percentage of the current Ask price to use for calculating the take profit level (default: 2.0)

## Global Variables

- **ticket**: The trade ticket number

## Custom Indicator Function

The `CustomIndicator` function is responsible for performing the supply and demand analysis and returning the entry zone based on the analysis. This is where you can customize the analysis algorithm according to your trading strategy.

## Expert Advisor Start Function

The `start` function is the entry point of the Expert Advisor. It first checks if there are any open trades using the `OrdersTotal` function. If there are open trades, the function returns without taking any further action.

Next, it checks if the current symbol and timeframe are supported. If not, the function returns.

The function then calculates the stop loss and take profit levels based on the user-defined parameters. It calls the `CustomIndicator` function to perform the supply and demand analysis and get the entry zone.

If the entry zone is valid (not equal to 0), the function opens a trade using the `OrderSend` function with the specified parameters. If the trade is opened successfully, the trade ticket is printed. Otherwise, an error message is printed with the corresponding error code.

## Expert Advisor Initialization Function

The `init` function is called during the initialization of the Expert Advisor. It is responsible for initializing necessary features and functions. In this example code, the function does not perform any specific initialization actions.

## Expert Advisor Deinitialization Function

The `deinit` function is called during the deinitialization of the Expert Advisor. It is responsible for performing any necessary cleanup actions. In this example code, the function does not perform any specific cleanup actions.
