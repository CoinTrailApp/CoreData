# Csv Header
```swift
let HEADER = [
    "Timestamp",
    "Transaction Type",
    "Asset",
    "Quantity Transacted",
    "Spot Price Currency",
    "Spot Price at Transaction",
    "Subtotal",
    "Total (inclusive of fees)",
    "Fees"
]
```
# Action Mapping
```swift
let ACTIONS = [
    "Buy":              AuditTransaction.Action.Buy,
    "Sell":             AuditTransaction.Action.Sell,
                
    "Receive":          AuditTransaction.Action.Deposit,
    "Send":             AuditTransaction.Action.Withdraw,
    "Convert":          AuditTransaction.Action.Swap,
                
    "Rewards Income":   AuditTransaction.Action.Earn,
    "Coinbase Earn":    AuditTransaction.Action.Reward
]
```

# Transaction Mapping
