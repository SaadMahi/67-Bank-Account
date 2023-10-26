# <div align='center'> 🏦 useReducer Bank Account 🏦 </div>
<p align="center">  <img src="https://github.com/SaadMahi/67-Bank-Account/assets/117567622/ec2b6ab5-fa27-4fc1-a433-d1aae937b66e" alt="useReducer bank account project"> </p>





## Overview

This project involves implementing a simple bank account system in React using the `useReducer` hook. The project requirements include modeling the state transitions of a bank account, including opening an account, depositing, withdrawing, requesting a loan, paying a loan, and closing an account. Several conditions and rules need to be followed during these operations.

### Condition Checking

- The project emphasizes the importance of condition checking in state management. Conditions are used to control the flow of operations such as deposit, withdrawal, loan request, and account closure. Conditions are crucial to ensuring that actions are only performed under specific circumstances.

### Immutable State Updates

- To maintain the immutability of the state in React, the project uses the spread operator (`...`) to create a new state object with the desired changes. This approach ensures that the original state remains unaltered, and the new state is returned as a result of the reducer function.

### User Interface Integration

- The project integrates the reducer-driven state management with the user interface. UI elements such as buttons are associated with specific actions, and the `dispatch` function is called when these buttons are clicked. The `disabled` attribute is used to control button accessibility based on the `isActive` state.

### Opening an Account

- The project demonstrates how to open a bank account by setting the `isActive` state to `true` and initializing the account with a minimum balance of 500. This operation showcases the use of the 'openAccount' action type.

### Depositing and Withdrawing

- The project illustrates how to deposit and withdraw money from the account. These operations are only allowed when the account is active (`isActive` is `true`). The 'deposit' and 'withdraw' action types are used for these operations.

### Requesting and Paying a Loan

- The project handles loan-related operations, such as requesting a loan and paying it back. A loan can only be requested if there is no existing loan. The 'requestLoan' action type is used for this purpose, and the loan amount is added to the account balance. To pay back a loan, the 'payLoan' action type is used, which deducts the loan amount from the balance.

### Closing an Account

- Account closure is implemented with the 'closeAccount' action type. An account can be closed only if there is no outstanding loan, and the balance is zero. This condition ensures that the account is deactivated, and all money is withdrawn.

### Handling Unspecified Action Types

- To maintain the robustness of the code, the project includes an error handling mechanism. If an unspecified or unknown action is encountered, an error is thrown.

```jsx
default:
  throw new Error('unknown');
