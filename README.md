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

Parameter：login(Account login).pwd(Password).symbol(Transaction symbol).op(0:Buy 1:Sell 2:BuyLimit 3:SellLimit).vo(Number of transactions).price(Transaction price).sp(Spread).sl(Stop loss).tp(Stop profit).type(0:demo 1:real)

Return value：code(0:success 1:fail).msg(success fail).Ticket(order number)

3》Close a position,

Function name：Tradeclose

Request method：Post

Parameter：login(Account login).pwd(Password).ticket(order number).type(0:demo 1:real)

Return value：code(0:success 1:fail).msg(success fail)

4》Modify order,

Function name：Trademodify

Request method：Post

Parameter：login(Account login).pwd(Password).ticket(order number).price(Transaction price).sp(Spread).sl(Stop loss).tp(Stop profit).ep(Expire).type(0:demo 1:real)

Return value：code(0:success 1:fail).msg(success fail)

5》Delete the list,

Function name：Tradedelete

Request method：Post

Parameter：login(Account login).pwd(Password).ticket(order number).type(0:demo 1:real)

Return value：code(0:success 1:fail).msg(success fail)

6》Account position,

Function name：Tradeopen

Request method：Post

Parameter：login(Account login).pwd(Password).type(0:demo 1:real)

Return value：code(0:success 1:fail).msg(success fail).Data(Order array)

7》Historical records,

Function name：Tradehis

Request method：Post

Parameter：login(Account login).pwd(Password).from(Start time).to(End time).type(0:demo 1:real)

Return value：code(0:success 1:fail).msg(success fail).Profit(reap profit).Data(Order array)

8》Trading hours,

Function name：TradeTime

Request method：Post

Parameter：login(Account login).pwd(Password).Symbol(Transaction symbol).Time(Trading hours).type(0:demo 1:real)

Return value：code(0:success 1:fail).msg(success fail)

9》Overnight interest,

Function name：GetSwap

Request method：Post

Parameter：Symbol(Transaction symbol).type(0:all 1:single)

Return value：Symbol(Transaction symbol).SwapLong(Inventory cost of sales order adjustment).SwapShort(Purchase order and adjust inventory fee)


The API described in this document provides various interfaces for MT4 trading, quotation and management,With our products,It can meet the needs of individual developers to write software for programming investment,You can also make customized development according to your business needs,Can also source code sales, welcome to discuss cooperation.
