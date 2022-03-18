# Transaction
```swift
struct AuditTransaction: Identifiable {
    let id: Int64
    let action: Action
    let amount: Amount
    let value: Value
    let settlementDate: Date
}
```
# Mapping
- Coinbase *exchange*
- Cashapp *payment*
- Celsius *Ce-Fi*
- Electrum *wallet*
