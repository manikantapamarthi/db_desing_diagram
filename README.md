# db_desing_diagram


# Tables

   1. Create tables named "customers", "accounts", and "transactions."
   
   2. Create foreign keys between accounts and customers using
the customer_id field.
   3. A Customer can have multiple Accounts.
   4. An Account can have multiple Transactions.

# Queries
   Displaying a ledger of transactions in a specific date range:
```Transaction.where(account_id: "10" and date >= "start_date" and date <= "end_date")```

  Calculate the balance by summing transaction_amounts for a specific
account_id:

```Transaction.where(account_id: "10").sum(:transaction_amount)```

Query the accounts table/collection to find accounts associated with the
customer's ID, then aggregate the balances.

```Account.where(customer_id: [1, 2, 3]).sum(:balance)```
