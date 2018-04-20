# 常見問題
Updated 20180419, ver >=v0.9.9

---
### How to reuse my account in a new/old book
1. Click DataMaintance > Export CSV
2. New a book, or go to new book, old book
3. Click DataMaintance > Import CSV > Working booking account.
WARN: Import CSV doesn't delete old data since v0.9.9, so if you need to clear the current book, Reset it first.


### How to import data from Financier
I don't really know how Finanicer doing in DB, However, I tried CSV way and it works, following are the steps.
1. In Financier,
    1. Run DataMaintance > Export CSV > All, it creates accounts.csv & details.csv in STORAGE/fsFinancier
2. In DM+ (v0.9.9)
    1. Go into DataMaintenance , Request storage permission if you don't have.
    2. Check the dm-folder location, it is usually the same parent as fsFinanicer, is like STORAGE/bwDailyMoney
    3. If you don't backup in DM+ ever, copy accounts.csv, details.csv to ./bwDailyMoney . if you ever do export csv in DM+, there should be a . /bwDailyMoney/csv/last folder, copy the 2 files to 'last' folder.
    4. Go to DataMaintenance again, execute Reset WorkingBook if there is any old data in the current book that you don't want to have.
    5. Click Import from CSV > Working-Book, it will append data in CSV to current working-book.
    6. Check to see everything is fine.



---
[導讀](../guide.md)<br/>
[如何使用](how2use.md)<br/>
[資料維護](data_maintenance.md)<br/>
[常見問題](faq.md)<br/>
[關於DM+](about.md)<br/>
[提供貢獻](contribution.md)<br/>
[贊助者徽章](sponsor_badge.md)<br/>
<br/>
如果DM+有幫助到你, 請[加加星星](https://play.google.com/store/apps/details?id=com.colaorange.dailymoney), ★★★★★.<br/>
[按讚DM+](https://www.facebook.com/co.daily.money)