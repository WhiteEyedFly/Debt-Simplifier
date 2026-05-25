Aim: Create code that can take a matrix (as seen below) of debts between any n people and simplify it such that the minimum number of payments need to be made for the minimum amount of money to resolve all debts.

Steps:
1. Validate the data and remove any debtors that have no debts and are owed no money
2. Remove any debts to oneself
3. If there are any pairs of people that both owe one another money, take the smallest of these debts and subtract it from the other to simplify
4. Transitivity of debt: if a owes b and b owes c, make simplify out the middle man
5. Distributivity of debt: if a and b owe x and y and a owes x the least, take the amount a owes to x from ax and by and add it to bx and ay
      Note: Distributivity doesn't reduce total debt paid but it can reduce the number of necessary transactions to resolve those debts
6. Clean up the data again, remove any now unnecessary columns and rows and clean floating errors

Input data (randomised for testing):
<img width="1897" height="637" alt="image" src="https://github.com/user-attachments/assets/54301e21-c9e7-41b9-9681-ba0c0c697aab" />

Output payment matrix:
<img width="1897" height="729" alt="image" src="https://github.com/user-attachments/assets/44885dd8-7a5e-4af8-baf6-b2332b434027" />


Report:
<img width="598" height="799" alt="image" src="https://github.com/user-attachments/assets/585032c5-3a13-43e3-a3bb-97a2ba459db4" />

The project has nested code up to four levels deep so works at O(n^4) with a matrix of 50 people in worst possible conditions taking 60 second to complete. It is intended for use personally so this upper limit poses no real issue at present.
