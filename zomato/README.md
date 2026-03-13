# Zomato App

A C++ implementation of a food delivery application inspired by Zomato, featuring order management, restaurant listings, user carts, and payment processing.

## Features

- **User Management**: Handle user accounts and profiles
- **Restaurant Management**: Add and manage restaurant listings with menus
- **Order Processing**: Support for delivery and pickup orders with scheduling options
- **Cart Functionality**: Add items to cart and manage orders
- **Payment Strategies**: Multiple payment methods including credit card and UPI
- **Notification Service**: Send notifications for order updates
- **Time Utilities**: Handle scheduling and time-based operations

## Project Structure

```
zomato/
├── main.cpp                 # Main application entry point
├── ZomatoApp.h              # Main application header
├── factories/               # Factory pattern for order creation
│   ├── OrderFactory.h
│   ├── NowOrderFactory.h
│   └── ScheduledOrderFactory.h
├── managers/                # Business logic managers
│   ├── OrderManager.h
│   └── RestaurantManager.h
├── models/                  # Data models
│   ├── Cart.h
│   ├── DeliveryOrder.h
│   ├── MenuItem.h
│   ├── Order.h
│   ├── PickupOrder.h
│   ├── Restaurant.h
│   └── User.h
├── services/                # Application services
│   └── NotificationService.h
├── strategies/              # Payment strategy pattern
│   ├── PaymentStrategy.h
│   ├── CreditCardPaymentStrategy.h
│   └── UpiPaymentStrategy.h
└── utils/                   # Utility functions
    └── TimeUtils.h
```

## Prerequisites

- C++ compiler (GCC, Clang, or MSVC)
- CMake (for build system)
- Standard C++ libraries

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd zomato
   ```

2. Create a build directory:
   ```bash
   mkdir build
   cd build
   ```

3. Configure with CMake:
   ```bash
   cmake ..
   ```

4. Build the project:
   ```bash
   make
   ```

## Usage

Run the application:
```bash
./zomato
```

The application provides a console-based interface for managing restaurants, users, and orders.

## Architecture

This application follows object-oriented design principles with the following patterns:

- **Factory Pattern**: For creating different types of orders (immediate and scheduled)
- **Strategy Pattern**: For implementing different payment methods
- **Manager Classes**: To handle business logic for orders and restaurants
- **Model Classes**: To represent data entities

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Build Notes

- Check `build_errors.txt` for any compilation issues
- The application uses standard C++ features and should compile on most modern compilers
- For Windows builds, ensure you have Visual Studio or MinGW installed

## Future Enhancements

- GUI interface
- Database integration
- Real-time order tracking
- Mobile app companion
- Advanced search and filtering
- Review and rating system