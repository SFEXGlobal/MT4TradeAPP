# MT4TradeAPP.NET
MT4 Trading API

Transaction API, based on the trading function of MT4, extends the trading function.

Functions include:

1》Account information,

Function name：TradeAcc

Request method：Post

Parameter：login(Account login).pwd(Password).type(0:demo 1:real)

Return value：Currency(Currency of account).Equity(Account equity on deposit).Balance(Account balance when money is deposited).Credit(Account deficit when money is deposited).Profit(The current profit of the account when the currency is deposited).Margin(Use of account deposit when deposited in currency).Freemargin(When money is deposited, the account can use margin)

2》Open a position or put up a bill,

Function name：Tradesend

Request method：Post

Parameter：login(Account login).pwd(Password).symbol(Transaction symbol).op(0:Buy 1:Sell 2:BuyLimit 3:SellLimit).vo(Number of transactions).price(Transaction price).sp(Spread).sl(Stop loss).tp().type(0:demo 1:real)

Return value：code(0:success 1:fail).msg(success fail).Ticket(order number)

3》Close a position,

Function name：Tradeclose

Request method：Post

Parameter：login(Account login).pwd(Password).ticket(order number).type(0:demo 1:real)

Return value：code(0:success 1:fail).msg(success fail)

4》
