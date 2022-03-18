# Csv Header
```swift
let HEADER = [
    "Internal id",
    "Date and time",
    "Transaction type",
    "Coin type",
    "Coin amount",
    "USD Value",
    "",     //Original Reward Coin"
    "",     //Reward Amount In Original Coin"
    "Confirmed"
]
```
# Action Mapping
```swift
let ACTIONS = [
    "Swap in" :             AuditTransaction.Action.Buy,
    "Swap out":             AuditTransaction.Action.Sell,

    "Transfer":             AuditTransaction.Action.Deposit,
    "Withdrawal":           AuditTransaction.Action.Withdraw,
    "Outbound Transfer":    AuditTransaction.Action.Withdraw,

    "Reward":               AuditTransaction.Action.Earn,
    "interest":             AuditTransaction.Action.Earn,
    "Promo Code Reward":    AuditTransaction.Action.Reward
]
```

# Transaction Mapping
