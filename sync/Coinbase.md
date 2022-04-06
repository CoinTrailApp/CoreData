# Json Response
```swift
struct JsonAccounts: Decodable {
    let pagination: JsonPagination
    let data: [JsonAccount]
}

struct JsonRecords: Decodable {
    let pagination: JsonPagination
    let data: [JsonRecord]
}

struct JsonAccount: Decodable {
    let id: String
    let balance: JsonBalance
    let primary: Bool
}

struct JsonRecord: Decodable, Identifiable, CustomStringConvertible {
    let id: String
    let type: String                // completed
    let status: String
    let amount: JsonBalance         // amout in COIN
    let native_amount: JsonBalance  // value in USD
    let created_at: String

    let trade: JsonTrade?
    let details: JsonDetails?
    //let transaction_fee: JsonBalance?   //network fee during transfer in COIN amount

    var description: String {
        return "{id: \(id), type: \(type), status: \(status), amount: \(amount.amount) \(amount.currency), native_amount: \(native_amount.amount) \(native_amount.currency), created_at: \(created_at)}"
    }
}

struct JsonBalance: Decodable {
    let amount: String
    let currency: String
}

//default 25 and < 100
struct JsonPagination: Decodable {
    let next_starting_after: String?
    let limit: Int
}

struct JsonDetails: Decodable {
    let header: String
    let subtitle: String
    let title: String
}

struct JsonTrade: Decodable {
    let id: String
}
```
# Action Mapping
```swift
let ACTIONS = [
    "buy":                  AuditTransaction.Action.Buy,
    "sell":                 AuditTransaction.Action.Sell,

    "receive":              AuditTransaction.Action.Deposit,
    "fiat_deposit":         AuditTransaction.Action.Deposit,
    "prime_deposit":        AuditTransaction.Action.Deposit,
    "exchange_withdrawal":  AuditTransaction.Action.Deposit,    //withdraw from CoinbasePro, prior to fiat_withdrawal

    "send":                 AuditTransaction.Action.Withdraw,
    "fiat_withdrawal":      AuditTransaction.Action.Withdraw,
    "prime_withdrawal":     AuditTransaction.Action.Withdraw,
    "exchange_deposit":     AuditTransaction.Action.Withdraw,   //deposit to CoinbasePro, orior to fiat_deposit

    "trade":                AuditTransaction.Action.Swap,

    "staking_reward":       AuditTransaction.Action.Earn,
    "inflation_reward":     AuditTransaction.Action.Earn,
    "interest":             AuditTransaction.Action.Earn
]
```

# Transaction Mapping
