# Enhanced Bank Management System with Transactions

A comprehensive C++ console application for managing bank client records with full CRUD operations and complete transaction management system.

## 🏦 Overview

This Enhanced Bank Management System is a console-based application written in C++ that demonstrates **Functional Programming** principles for managing bank client accounts with advanced transaction capabilities. The system uses file-based storage to persist client data and provides a user-friendly dual-menu interface.

### 🎯 Programming Paradigm

This version of the system is built using **Functional Programming** approach, featuring:
- **Function-based architecture** with clear separation of concerns
- **Pure functions** for data transformation and validation
- **Stateless operations** with data passed between functions
- **Procedural flow** with structured programming techniques
- **Modular transaction system** with dedicated menu handling

### 🔄 Future Development

An **Object-Oriented Programming (OOP)** version of this system is planned for development, which will include:
- **Class-based design** with proper encapsulation (Account, Client, Transaction classes)
- **Inheritance hierarchies** for different account types (Savings, Checking, etc.)
- **Polymorphism** for flexible client and transaction management
- **Design patterns** implementation (Factory, Strategy, Observer, etc.)
- **Better code reusability** and maintainability

This functional version serves as a foundation and reference point for comparing programming paradigms and understanding the evolution from procedural to object-oriented design.

## 🆕 What's New in This Version

This enhanced version builds upon the basic bank management system with significant improvements and new functionality:

> 📌 **Want to see the original version?** Check out the [Basic Bank Management System](https://github.com/yourusername/bank-management-functional-cpp) to compare the evolution and understand the development journey from basic CRUD operations to a complete banking solution.

### ✨ Major Additions & Enhancements

#### 🆕 **New Transaction Management System**
- **Complete Transaction Menu**: Dedicated menu system for financial operations
- **Deposit Functionality**: Add money to client accounts with validation
- **Withdrawal System**: Remove money with balance checking and overdraft protection
- **Total Balance Calculator**: View individual and system-wide balance summaries
- **Transaction Confirmations**: Safety prompts for all financial operations

#### 🔧 **Enhanced User Interface**
- **Dual Menu System**: Main menu + dedicated transactions menu
- **Improved Navigation**: Seamless switching between menus
- **Better Error Handling**: Enhanced validation for insufficient funds
- **Cleaner Display**: Formatted balance views and transaction screens

#### 🛡️ **Advanced Validation**
- **Balance Verification**: Prevents withdrawals exceeding account balance
- **Account Existence Check**: Validates account before transactions
- **Amount Validation**: Ensures positive transaction amounts
- **Real-time Balance Updates**: Immediate reflection of changes

### 📊 **Comparison with Basic Version**

| Feature | Basic Version | Enhanced Version |
|---------|---------------|------------------|
| **Menus** | Single main menu | Dual menu system (Main + Transactions) |
| **Options** | 6 options (1-6) | 7 main options + 4 transaction options |
| **Financial Operations** | ❌ None | ✅ Deposit, Withdraw, Balance Summary |
| **Balance Management** | View only | Full transaction capabilities |
| **Validation** | Basic input validation | Advanced financial validation |
| **User Experience** | Simple CRUD | Complete banking simulation |
| **Code Structure** | ~400 lines | ~600+ lines with transaction logic |

## ✨ Core Features

### 👥 Client Management (Inherited from Basic Version)
- **Client List Display**: View all registered clients with their details in a formatted table
- **Add New Clients**: Register new clients with validation for duplicate account numbers
- **Delete Clients**: Remove client records with confirmation prompts
- **Update Client Info**: Modify existing client information
- **Find Clients**: Search for specific clients by account number

### 💰 Transaction Management (🆕 NEW)
- **Deposit Money**: Add funds to client accounts with confirmation
- **Withdraw Money**: Remove funds with balance validation and overdraft protection
- **Total Balances**: View all client balances and calculate total system balance
- **Transaction Validation**: Ensures sufficient funds and prevents invalid operations

### 🔒 Security & Validation (Enhanced)
- **Account Number Uniqueness**: Prevents duplicate account numbers
- **Balance Verification**: Validates sufficient funds before withdrawals
- **Confirmation Prompts**: Requires confirmation for all critical operations
- **Data Integrity**: Maintains consistent file-based storage
- **Transaction Safety**: Multiple validation layers for financial operations

## 🗂️ Data Structure

Each client record contains:
- **Account Number**: Unique identifier for each client
- **PIN Code**: Client's personal identification number
- **Name**: Full name of the client
- **Phone**: Contact phone number
- **Account Balance**: Current balance in the account

## 🚀 Getting Started

### Prerequisites

- C++ compiler (GCC, MSVC, or Clang)
- Standard C++ libraries
- Windows OS (due to `system("cls")` and `system("pause>0")` commands)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/enhanced-bank-system-functional.git
   cd enhanced-bank-system-functional
   ```

2. **Compile the program**
   ```bash
   g++ -o bank_system main.cpp
   ```

3. **Run the application**
   ```bash
   ./bank_system
   ```

## 📋 Usage

### Main Menu Options

When you run the program, you'll see a main menu with the following options:

1. **Show Client List** - Displays all clients in a formatted table
2. **Add New Client** - Add one or more new clients to the system
3. **Delete Client** - Remove a client by account number
4. **Update Client Info** - Modify existing client information
5. **Find Client** - Search for a client by account number
6. **Transactions** - Access the transaction management menu
7. **Exit** - Close the application

### Transaction Menu Options

The transaction menu provides:

1. **Deposit** - Add money to a client's account
2. **Withdraw** - Remove money from a client's account (with balance validation)
3. **Total Balances** - View all client balances and system total
4. **Main Menu** - Return to the main menu

### Sample Transaction Flow

#### Making a Deposit:
```
Please enter AccountNumber? A101
Account found - Client: John Doe
Current Balance: $5000.00

Please enter deposit amount? 1500
Are you sure you want to perform this transaction? y/n? y
Done Successfully, New balance is: $6500.00
```

#### Making a Withdrawal:
```
Please enter AccountNumber? A101
Account found - Client: John Doe
Current Balance: $6500.00

Please enter withdraw amount? 2000
Are you sure you want to perform this transaction? y/n? y
Done Successfully, New balance is: $4500.00
```

### Sample Data Format

The system stores data in `Clients.txt` with the following format:
```
A101#//#1234#//#John Doe#//#+1234567890#//#6500.00
A102#//#5678#//#Jane Smith#//#+0987654321#//#7500.50
A103#//#9012#//#Bob Johnson#//#+1122334455#//#3200.75
```

## 🏗️ Code Structure

### Core Client Management Functions
- `ShowMainMenue()` - Displays the main menu and handles user navigation
- `LoadCleintsDataFromFile()` - Reads client data from file into memory
- `SaveCleintsDataToFile()` - Writes client data from memory to file
- `ConvertLinetoRecord()` - Converts file line to client structure
- `ConvertRecordToLine()` - Converts client structure to file line
- `FindClientByAccountNumber()` - Searches for a client by account number

### 🔍 **Detailed Code Changes**

#### **New Functions Added:**
- `ShowTransactionsMenue()` - Complete transaction menu system
- `DepositBalanceToClientByAccountNumber()` - Core deposit logic with confirmation
- `ShowDepositScreen()` - User interface for deposit operations
- `ShowWithDrawScreen()` - User interface for withdrawal with validation
- `ShowTotalBalance()` - System-wide balance calculation and display
- `PrintClientRecordBalanceRecordLine()` - Formatted balance display
- `ReadTransactionsMenueOptions()` - Transaction menu input handling
- `PerformTransactionsMenueOptions()` - Transaction menu navigation
- `GoBackToTransactionMenue()` - Navigation helper for transaction menu

#### **Modified Functions:**
- `ShowMainMenue()` - Updated to include Transactions option (6) and shifted Exit to (7)
- `PerfromMainMenueOption()` - Added case for new transaction menu
- `ReadMainMenueOption()` - Updated range from [1-6] to [1-7]

#### **New Enumerations:**
```cpp
enum enTransactionsMenueOptions {
    eDeposit = 1, Withdraw = 2,
    eTotalBalances = 3, eMainMenue = 4
};
```

#### **Enhanced Enumerations:**
```cpp
enum enMainMenueOptions {
    eListClients = 1, eAddNewClient = 2,
    eDeleteClient = 3, eUpdateClient = 4,
    eFindClient = 5, eTransactions = 6, eExit = 7  // Added eTransactions, shifted eExit
};
```

### 📈 **Lines of Code Growth:**
- **Basic Version**: ~450 lines
- **Enhanced Version**: ~650+ lines
- **Growth**: ~200+ lines of new functionality
- **New Features**: 40% increase in codebase

### Key Enumerations
```cpp
enum enMainMenueOptions {
    eListClients = 1, eAddNewClient = 2,
    eDeleteClient = 3, eUpdateClient = 4,
    eFindClient = 5, eTransactions = 6, eExit = 7
};

enum enTransactionsMenueOptions {
    eDeposit = 1, Withdraw = 2,
    eTotalBalances = 3, eMainMenue = 4
};
```

### Key Structures
```cpp
struct sClient {
    string AccountNumber;
    string PinCode;
    string Name;
    string Phone;
    double AccountBalance;
    bool MarkForDelete;
};
```

## 📁 File Structure

```
enhanced-bank-system-functional/
│
├── main.cpp           # Main source code file
├── Clients.txt        # Client data storage (auto-generated)
├── README.md          # This file
└── .gitignore         # Git ignore file
```

## 🔒 Security Features

- **Account Number Validation**: Prevents duplicate account numbers
- **Balance Verification**: Ensures sufficient funds before withdrawals
- **Confirmation Prompts**: Requires confirmation before all transactions
- **Data Integrity**: Uses structured file format to maintain consistency
- **Input Validation**: Validates all user inputs for correctness

## 🛠️ Future Enhancements

- [ ] Add transaction history logging and reporting
- [ ] Implement password protection for system access
- [ ] Add data encryption for sensitive information
- [ ] Create interest calculation features
- [ ] Add transfer money between accounts functionality
- [ ] Implement account types (Savings, Checking, Credit)
- [ ] Create a GUI version using Qt or similar framework
- [ ] Add database support (MySQL/SQLite) instead of file-based storage
- [ ] Implement user roles and permissions (Admin, Teller, etc.)
- [ ] Add data backup and restore functionality
- [ ] Include comprehensive reporting features (CSV, PDF exports)
- [ ] Add audit trail for all transactions
- [ ] Implement account freezing/unfreezing capabilities

## 🔗 Related Projects

This project is part of a series demonstrating different programming paradigms:

### 📂 **Project Evolution Timeline:**
1. **[Basic Bank Management System](https://github.com/AbdelhamidSherif/bank-management-functional-cpp)** - The original functional programming version with basic CRUD operations
2. **Current Project** - Enhanced version with complete transaction management
3. **Coming Soon** - Object-Oriented Programming (OOP) version for paradigm comparison

### 🔄 **Quick Navigation:**
- 🏃‍♂️ **[Go to Basic Version →](https://github.com/AbdelhamidSherif/bank-management-functional-cpp)** - Simple client management without transactions
- 🚀 **[View OOP Version →](https://github.com/AbdelhamidSherif/bank-system-oop-cpp)** - Coming soon with class-based design
- 📚 **[See All Banking Projects →](https://github.com/AbdelhamidSherif?tab=repositories&q=bank&type=&language=)** - Complete collection

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Steps to Contribute

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/TransactionHistory`)
3. Commit your changes (`git commit -m 'Add transaction history feature'`)
4. Push to the branch (`git push origin feature/TransactionHistory`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Abdelhamid Sherif**
- GitHub: [@AbdelhamidSherif](https://github.com/AbdelhamidSherif)
- LinkedIn: [abdelhamid-sherif](https://linkedin.com/in/abdelhamid-sherif)

## 📞 Support

If you have any questions or need help with the system, please:
1. Check the existing issues in the repository
2. Create a new issue with a detailed description
3. Contact the maintainer directly

## 🙏 Acknowledgments

- Thanks to all contributors who have helped improve this project
- Inspired by real-world banking systems and best practices in C++ development
- Educational project demonstrating functional programming principles

---

⭐ If you found this project helpful, please give it a star on GitHub!
