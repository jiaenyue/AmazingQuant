# Trade Center Module

The `trade_center` module is responsible for handling all aspects of the trading process, from order creation and management to execution and risk assessment. It is an event-driven system that processes trading events to ensure that orders are handled correctly and efficiently.

## Core Components

The module is composed of several key components, each handling a specific part of the trade lifecycle:

- **`event_order.py`**: This component manages order-related events. Its responsibilities include:
  - Validating new orders.
  - Checking for sufficient available capital before placing a buy order.
  - Verifying that there are enough shares available to sell for a sell order.
  - Adjusting order quantities to meet lot size requirements.

- **`event_risk_management.py`**: Before an order is sent to the market, it goes through a series of risk checks defined in this component. This includes:
  - **Blacklist Check**: Verifying that the instrument is not on a list of restricted securities.
  - **Order Status Update**: Modifying the order status if it fails any risk checks.
  - **Order Dispatch**: Sending the order for execution if it passes all risk assessments.

- **`event_deal.py`**: This component handles the events that occur after a trade has been executed. Its functions include:
  - **Slippage and Commission Calculation**: Adjusting the trade price to account for slippage and applying commission fees.
  - **Position Updates**: Updating the portfolio's position list to reflect the new trade, including average price and quantity.
  - **Account Updates**: Adjusting the available cash in the trading account based on the trade's value.

- **`trade.py`**: This is the central component that likely orchestrates the trading process, coordinating the actions of the other event handlers to manage the end-to-end flow of a trade.

Together, these components form a robust system for managing trades within the AmazingQuant framework, ensuring that all trading activities are processed in a structured and risk-aware manner.