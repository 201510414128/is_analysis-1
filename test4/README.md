# 实验4：图书管理系统顺序图绘制
|学号|班级|姓名|照片|
|:-------:|:-------------: | :----------:|
|201510414113|软件(本)15-1|江自杰|

## 图书管理系统的顺序图

## 1. 借书用例
## 1.1. 借书用例PlantUML源码

``` sequence
@startuml
actor  借书者 as lender
actor  图书管理员 as bookAdmin
activate lender
activate bookAdmin
lender->bookAdmin:提供自身id
lender->bookAdmin:提供借书id
deactivate lender
bookAdmin->图书管理系统:login()
activate 图书管理系统
bookAdmin->图书管理系统:1.checkLend(int lendId):查询借书者身份
bookAdmin->图书管理系统:2.checkBook(int bookId):查询所借书籍是否可借
bookAdmin<-图书管理系统:result():true or false
deactivate bookAdmin
activate lend
图书管理系统->lend:3.getLender(int lendId)
图书管理系统<-lend:result():true or false
activate book
图书管理系统->book:4.getLendBook(int bookId)
图书管理系统<-book:result():true or false
图书管理系统->book:5.reduceBook(int bookId)
deactivate book
图书管理系统->lend:5.updateLend(int lendId,int bookId)
deactivate lend
图书管理系统->lender:result
activate lender
deactivate lender
deactivate 图书管理系统
@enduml
```
## 1.2. 借书用例顺序图
![class](1.png)

## 1.3. 借书用例顺序图说明
```
1. login()：图书管理员登录
2. checkLend(int lendId)：查询借书者的身份是否存在
3. checkBook(int bookId)：查询所借书籍是否存在
4. result()：返回查询的结果：true or false;
5. getLender(int lendId)：获取借书者身份
6. getLendBook(int bookId)：获取所借图书
7. reduceBook(int bookId)：减少所借图书的数量
8. updateLend(int bookId,int lendId)：修改借书者的借书记录
  ```
  
  ## 2. 还书用例
## 2.1. 还书用例PlantUML源码

``` sequence
@startuml
actor  还书者 as returnBook
actor  图书管理员 as bookAdmin
activate returnBook
activate bookAdmin
returnBook->bookAdmin:提供自身id
returnBook->bookAdmin:提供借书id
deactivate returnBook
bookAdmin->图书管理系统:login()
activate 图书管理系统
bookAdmin->图书管理系统:1.checkReturn(int returnId):查询还书者身份
bookAdmin->图书管理系统:2.checkBook(int bookId):查询所还书籍是否属于该图书馆
bookAdmin<-图书管理系统:result():true or false
deactivate bookAdmin
activate _return
图书管理系统->_return:3.getReturner(int returnId)
图书管理系统<-_return:result():true or false
图书管理系统->_return:4.updateReturn(int lendId,int bookId)
deactivate _return
activate book
图书管理系统->book:5.getReturnBook(int bookId)
图书管理系统<-book:result():true or false
图书管理系统->book:6.addBook(int bookId)
deactivate book
activate lend
图书管理系统->lend:7.updateLend(int lendId,int bookId)
deactivate lend
activate returnBook
图书管理系统->returnBook:result
deactivate returnBook
deactivate 图书管理系统
@enduml
```

## 2.2. 还书用例顺序图
![class](2.png)

## 2.3. 还书用例顺序图说明
```
1. login()：借阅者提供还书书籍，管理员登陆该系统的函数。
2. getBookInfo()：扫描该书籍的书号，获取相关图书信息的函数。
3. getBorrowInfo()：获取借阅记录的信息的函数。
4. getBorrowDate()：获取借阅该书籍的日期的函数。
5. getNowDate()：获取当前时间的日期的函数。
6. isOverTime()：判断该借阅者的借书时间是否超时的函数。
7. builtReturnInfo()：创建还书记录的函数。
8. updateBookInfo()：更新图书馆里的书籍信息的函数，标记该图书的状态为可借。
9. updateReaderInfo()：更新读者的还书信息的函数。
10. record()：记录借阅者的逾期记录的函数。
11. return：返回还书成功。
```
