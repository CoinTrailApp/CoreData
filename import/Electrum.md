# Csv Header
```swift
let HEADER = [
    "transaction_hash",
    "label",
    "confirmations",
    "value",
    "fiat_value",
    "fee",
    "fiat_fee",
    "timestamp"
]
```
# Action Mapping
```swift
let ACTIONS = [
    "$value > 0":  AuditTransaction.Action.Deposit,
    "$value < 0":  AuditTransaction.Action.Withdraw
]
```

# Transaction Mapping
