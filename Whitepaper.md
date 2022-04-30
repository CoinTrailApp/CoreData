# Abstract
High demand in cryptocurrency creates a new tax filing challenge for individuals who own this asset class. Unlike, traditional finance where an institution can hand out 8949 tax form at the end of the year, the crypto exchanges are not able to do so due to lack of origin Cost Basic when assets being transferred cross exchanges.

In this paper, CoinTrail is proposing a very simple and effectively algorithm to keep track of Cost Basic and Tax Calculation engine which helps easy the mind of crypto HODLers.

# Introduction
Unlike existing solutions on the market with SAS based approach, CoinTrail is a Crypto Tax Calculator in your pocket, an iOS app that runs locally on the mobile device. With no server, no backend, no signup...totally will ensure privacy of asset owners and offer better user experience.

TBD...

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

# Tax Calculator Engine
TBD

