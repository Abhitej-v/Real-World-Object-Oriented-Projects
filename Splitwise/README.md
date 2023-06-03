## Design Splitwise

## Requirements and test cases:

refer the below link for requirements and test cases of this design

[Design Splitwise | Machine Coding Round Questions (SDE I/II)](https://workat.tech/machine-coding/practice/splitwise-problem-0kp2yneec2q2)

## 

## Class responsibilities:

SplitStrategyManager: responsible for choosing the bill splitting strategy based on the user input of split format.

SplitManager: To get the split strategy from  SplitStrategyManager and trigger API call on the strategy to split the bill.

UserManager: Has all the users that are created. It is responsible for triggering the API's of diplayLedger in user class. Method overloading is used for show() functionality to display balance of all user or display balance of single user.

User : User "has a" ledger. User is mainly responsible for updating its ledger and performing operation on its ledger.

Ledger: Unlike conventional ledger the ledger object in this design doesn't have anything like a debit or credit column. It has a Map that stores the user and the corresponding balance with that user. If the value is negative then we have to pay to the user. if the value is positive then he user pays us. read and write operations of this Map.

SplitStrategy: it's an interface which is implemented by PercentSplitStrategy, EqualSplitStrategy, ExactSplitStrategy. This interface is responsible for distributeExpense implementation. depending upon the type of split format that strategy is chosen and the ledger of users is updated. The validation criterion is different for different strategy hence the isValid method is private and specific to the respective strategies.

ExpenseMetaData: Contains information about the expense.

## 

## Design, Code and testing walkthrough:

Gdrive Link for the video: https://drive.google.com/file/d/1-MMQSV_JqTySG0EHu9zgOmkl89suA8YF/view?usp=sharing

Note: The design pattern I used is strategy design pattern. At run time depending upon the input the split bill logic varies. So due to that reasoning I stated it as strategy design pattern but it also very similar to factory design pattern as well. Objects are created like how they are created in simple factory pattern. Regardless of the object that's created the distributeExpense responsibility is delegated to that object.



Linkdin: https://www.linkedin.com/in/abhitej-voruganti-596a181b2/



