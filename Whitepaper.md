# Transaction
```swift
struct AuditTransaction: Identifiable {
    let id: Int64
    let action: Action
    let amount: Amount
    let value: Value
    let settlementDate: Date
}

enum Action: Enumeration {
    case Reward
    case Earn
                
    case Buy
    case Sell
                
    case Deposit
    case Withdraw
                
    case Swap 
}
```

# Basic cost
TBD

# Mapping
- Coinbase *exchange*
- Cashapp *payment*
- Celsius *Ce-Fi*
- Electrum *wallet*
