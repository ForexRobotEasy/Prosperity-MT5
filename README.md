# Prosperity MT5

Prosperity MT5 is a trading robot developed by the Forex Robot Easy Team. It is designed to execute buy and sell trades automatically on the MetaTrader 5 platform. This ReadMe file provides an overview of the code and explains how the robot works.

## Code Description

The code provided is written in MQL5, the programming language used for developing trading robots on the MetaTrader 5 platform. Here is a breakdown of the code and its functionality:

### Input Parameters

The code begins by defining input parameters that can be adjusted by the user:

- `TakeProfit`: The desired take profit level in pips.
- `StopLoss`: The desired stop loss level in pips.
- `LotSize`: The desired lot size for each trade.

### Global Variables

A global variable `ticket` is declared to store the ticket number of the executed trade.

### OnTick Function

The `OnTick()` function is the main function that is called on every tick of the price. Here is a step-by-step breakdown of the function:

1. Check if the trade context is not busy. If it is busy, it means that there is an ongoing trade and we cannot open a new position at the moment. Therefore, the function exits without executing any trade.
2. If the trade context is not busy, check if there are no open positions.
3. If there are no open positions, generate a buy trade using the `OrderSend()` function. The function accepts parameters such as the symbol, trade type (buy or sell), lot size, entry price, stop loss and take profit levels, trade comment, and color for the trade label on the chart.
4. Check if the buy trade was executed successfully by checking if the returned ticket number is greater than 0. If it is greater than 0, print a success message with the ticket number. If it is not greater than 0, print an error message with the error code.
5. If there are open positions, generate a sell trade using the same `OrderSend()` function as before, but with the trade type set to sell.
6. Check if the sell trade was executed successfully and print the corresponding success or error message.

### OnDeinit Function

The `OnDeinit()` function is called upon deinitialization of the robot. It is responsible for closing any open positions before the robot is removed from the chart.

## Product Description

Prosperity MT5 is a high-growth Forex robot with low drawdown. It is designed to automatically execute trades on the MetaTrader 5 platform, allowing users to potentially profit from the Forex market without the need for manual intervention.

This product is not developed or endorsed by ForexRobotEasy. The code provided in this ReadMe file serves as a sample code that can work similarly to the Prosperity MT5 robot. For the official developer and more information about the product, please visit the [Prosperity MT5 Review](https://forexroboteasy.com/forex-robot-review/prosperity-mt5-review-high-growth-forex-bot-with-low-draw-down/) on ForexRobotEasy's website.

Please note that trading robots involve risks, and past performance is not indicative of future results. It is recommended to fully understand the functionality and risks of any trading robot before using it in live trading.
