# Csv Header
```swift
let HEADER = [
  "portfolio",
  "type",                 // action
  "time",
  "amount",               // amount
  "balance",
  "amount/balance unit",  // asset
  "transfer id",
  "trade id",
  "order id"              // refid
]
```
# Action Mapping
```swift
let ACTIONS = [
    "transfer":     AuditTransaction.Action.Withdraw | Deposit,
    "match":        AuditTransaction.Action.Sell | Buy,
                
    "withdrawal":   AuditTransaction.Action.Withdraw,
    "deposit":      AuditTransaction.Action.Deposit,
    
    "fee":          AuditTransaction.Action.Swap,
    "conversion":   AuditTransaction.Action.Swap,
    "rebate":       AuditTransaction.Action.Reward
]
```

# Transaction Mapping
