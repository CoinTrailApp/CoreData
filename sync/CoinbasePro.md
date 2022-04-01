# Json Response
```swift
struct JsonAccount: Decodable {
    let id: String
    let currency: String
    let trading_enabled: Bool
}

struct JsonRecord: Decodable, CustomStringConvertible {
    let id: String
    let currency: String?  //not available until fetched
    let amount: String
    let type: String
    let details: JsonDetails
    let created_at: String

    var description: String {
        return "{id: \(id), amount: \(amount), currency: \(currency ?? "?"), type: \(type), created_at: \(created_at), details: \(details)}"
    }
}

struct JsonDetails: Decodable, CustomStringConvertible {
    let order_id: String?
    let transfer_id: String?

    var description: String {
        return "{order_id: \(order_id ?? ""), transfer_id: \(transfer_id ?? "")}"
    }
}
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
