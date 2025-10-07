# Utils Module

The `utils` module provides a collection of utility functions that support various operations across the AmazingQuant platform. These utilities handle tasks such as data management, logging, database connections, and more.

## Core Utilities

This module includes the following key utility files:

- **`get_data.py`**: Contains functions for retrieving data from local storage. This is used to load datasets required for backtesting and analysis.
- **`save_data.py`**: Provides functions for saving data, such as strategy results or processed datasets, to local storage.
- **`data_transfer.py`**: Includes tools for transferring data between different formats or systems.
- **`code_transfer.py`**: Contains functions for converting or mapping security codes and other identifiers.
- **`transfer_field.py`**: Utilities for mapping or transforming data fields.
- **`logger.py`**: A logging utility to record events, errors, and other important information during the execution of trading strategies. This is crucial for debugging and monitoring.
- **`mongo_connection_me.py` & `mongo_connection_pm.py`**: These files manage connections to MongoDB databases, likely for different environments or purposes (e.g., market data vs. portfolio management data).
- **`generate_random_id.py`**: A function to generate unique random identifiers, which can be used for orders, trades, or other entities that require a unique ID.
- **`security_type.py`**: Defines constants or enums for different types of securities (e.g., stocks, futures).
- **`singleton.py`**: An implementation of the Singleton design pattern, used to ensure that a class has only one instance.
- **`performance_test.py`**: Tools for conducting performance tests on different parts of the system.

These utilities are essential for the smooth operation of the platform, providing the foundational services needed to build and run complex quantitative trading strategies.