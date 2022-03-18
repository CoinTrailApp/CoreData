# Csv Header
```swift
let HEADER = [
    "", //Transaction ID
    "Date",
    "Transaction Type",
    "Currency",
    "Amount",
    "Fee",
    "Net Amount",
    "Asset Type",
    "Asset Price",
    "Asset Amount",
    "Status",
    "Notes",
    "Name of sender/receiver",
    ""  //Account
]
```
# Action Mapping
```swift
let ACTIONS = [
    "Bitcoin Buy":          AuditTransaction.Action.Buy,
    "Bitcoin Sale":         AuditTransaction.Action.Sell,

    "Bitcoin Deposit":      AuditTransaction.Action.Deposit,
    "Bitcoin Withdrawal":   AuditTransaction.Action.Withdraw,

    "Bitcoin Boost":        AuditTransaction.Action.Reward,
    "Bitcoin Reward":       AuditTransaction.Action.Earn
]
```

# Transaction Mapping
