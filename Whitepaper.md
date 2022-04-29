# Abstract
High demand in cryptocurrency is creating a new tax filing challenge for individuals who own this asset class. Unlike, traditional finance where an institution can hand out 8949 tax form at the end of the year, the crypto exchanges are not able to do so due to lack of origin Cost Basic when assets being transferred cross exchanges.

In this paper, CoinTrail is proposing a very simple and effectively algorithm to keep track of Cost Basic and Tax Calculation engine which helps easy the mind of crypto HODLers.

# Introduction

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

# Tax Engine
TBD

