# HOW TO USE
Updated 20180419, ver >=v0.9.9

---
## Concept
The concept of daily money is very simple
> 1. Different accounts (you create accounts depends on your case)
> 2. Money transaction between accounts. (you record detail for each transaction)

## Accounts
There are 5 types account, you can create/edit/delete it in Account Manager page.
> 1. <span style="color:#2AAF52">Income : salary etc..</span>
> 2. <span style="color:#BF5A75">Expense : food, entertainment etc.</span>
> 3. <span style="color:#B69134">Asset : cash, bank</span>
> 4. <span style="color:#7A65BF">Liability : credit card, loan.</span>
> 5. <span style="color:#31A0CF">Other : ...like a asset but is not asset.</span>

* To sort your account, you just add 1,2,.. or A.B,.. as the prefix of name of account. <br/>
* Account name could have a hierarchical by naming with .(dot), Ex: Food.lunch, Food.dinner . When editing transaction detail, it provides better selecting of account.

## The transaction detail
When you spent money then you can click the Add Detail on the Main page to create a new record.
For example, when you spent $10 bought a meal, in Detail Editor page, you do
> 1. <span style="color:#B69134">Select from account : Cash</span>
> 2. <span style="color:#BF5A75">Select to account : Food</span>
> 3. Select date : today
> 4. Input money by calculator : 10
> 5. Input description : hot dog, coke.
> 6. Click Create then click Close if no more transaction needs to be created.

this is a just very common use case of daily-money, but, what if your salary is deposit to bank directly, you use credit card buy books on internet? daily-money provide different type of account s, and you could create various accounts against 5 account type.
Use cases

_Salary to Bank_
> <span style="color:#2AAF52">From : Salary </span><br/>
> <span style="color:#B69134">To : Bank <span><br/>

_Bank to Cash_
> <span style="color:#B69134">From : Bank </span><br/>
> <span style="color:#B69134">To : Cash </span><br/>

_Buy stuff by credit card_
> <span style="color:#7A65BF">From : Credit card </span><br/>
> <span style="color:#BF5A75">To : Expensive 3C </span><br/>

_Pay credit card bill by Cash_
> <span style="color:#B69134">From : Cash </span><br/>
> <span style="color:#7A65BF">To : Credit card </span><br/>

## Balance Reports

### Ranged Balance
In ranged balance reports, I count balance of all the details that you created. The balance is calculated in a time range
(current week, current month, current year, or you can change to other range by click the arrow button)

### Cumulated Balance
To calculate cumulated balance (ex, how much cash I have now, how much liability I have now. not how much I spent this week),
you have to set a initial value to a account
(generally <span style="color:#B69134">Asset</span> or <span style="color:#7A65BF">Liability</span> type accounts have non-zero initial value.
<span style="color:#2AAF52">Income</span> and <span style="color:#BF5A75">Expense</span> type account should have no initial value).

If you forgot to set initial value of an account, there is a simple way to adjust it.
For example , "I have cash 333, but cumulated balance reports shows I have cash -100)
> 1. Edit <span style="color:#B69134">Cash account</span>
> 2. Set initial value of cash to 433, result of (333 - (-100))

## Multiple Books
You can create multiple-books and active one book as the 'Working-Book'. You can define a currency symbol (ex, '$','¥'..etc)
and the position of the symbol of a book. After you created a book, application will allocate another database to store
accounts and details, data between books are not able to be transfer since they are isolated.

When exporting current data to CSV, it will export two files, details.csv and accounts.csv, which are sharing between
all books, and another two files,details-'id'.cvs and accounts-'id'.csv, 'id' is the book id),for working book only,
When importing data from CSV, you can choose to import from shared or non-shared file.

If you delete a book, the database of that book will also be delete (included accounts and details),
the default book(id = 0) and current working book are not delete-able,

---
[Guide](../guide.md)<br/>
[How to use](how2use.md)<br/>
[Data Maintenance](data_maintenance.md)<br/>
[FAQ](faq.md)<br/>
[About DM+](about.md)<br/>
[Contribution](contribution.md)<br/>
[Sponsor Badge](sponsor_badge.md)<br/>
<br/>
If DM+ helped you, go to [vote DM+](https://play.google.com/store/apps/details?id=com.colaorange.dailymoney), ★★★★★.<br/>
[Like and poke DM+](https://www.facebook.com/co.daily.money)