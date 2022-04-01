# Json Response
```swift
struct JsonRecords: Decodable {
    let pagination: JsonPagination
    let record: [JsonRecord]
}

struct JsonRecord: Decodable, CustomStringConvertible {
    let id: String
    let amount_precise: String
    let amount_usd: String
    let coin: String
    let nature: String
    let time: String
    let state: String

    var description: String {
        return "{id: \(id), amount_precise: \(amount_precise), amount_usd: \(amount_usd), coin: \(coin), nature: \(nature), time: \(time), state: \(state)}"
    }
}

struct JsonPagination: Decodable {
    let current: Int
    let pages: Int
}
```
# Action Mapping
```swift
let ACTIONS = [
    "swap_in" :             AuditTransaction.Action.Buy,
    "swap_out":             AuditTransaction.Action.Sell,

    "deposit":              AuditTransaction.Action.Deposit,
    "withdrawal":           AuditTransaction.Action.Withdraw,
    "outbound_transfer":    AuditTransaction.Action.Withdraw,

    "reward":               AuditTransaction.Action.Earn,
    "interest":             AuditTransaction.Action.Earn,
    "promo_code_reward":    AuditTransaction.Action.Reward
]
```

# Transaction Mapping
