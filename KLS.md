# KLS

### Remote desktop to 10.102.34.222

```
.\klsadmin
Kls@d18$
Password@!!!###
```



### Export report (Before EOD)

1. LN051T
   - Navigate to MIS Report > General ledger report > LN051T
   - Click “Init ” and select criteria as below
   ```
   Branch : Head Office
   To Date : Current Date 
   Business : All
   Product : All
   Port transfer : All
   ```
   - Accept
   - Export
   - Close
     
2. LN803
   - Navigate to MIS Report > Credit report > LN803
   - Click “Init ” and select criteria as below
   ```
   Business: All
   From Date : 01/01/2022 - Current date
   To date : Current Date 
   Loan Origination Status : All
   Branch : Head Officer
   ```
   - Accept
   - Export
   - Close
     
### Copy File
>C:\client_pro\EXCELOUTPUT\ "FILE NAME" TO C:\Daily report_KLS
   ```
   00435_LN051T_2039.txt
   000435_LN803_2046.XLS
   ```
### Exit WISE KLS 

### Remote to "10.100.13.10"
```
wiseadmin
Wi$e@dm1n
Wi$e@dmin724
Wi$e@Kls724
```

### Run Batch
   1.  Check D storage should be at least 350 GB
   2.  Screenshot of Storage 
   3.  Restart Service SQL Server. (Must run every time before run batch)
   4.  Service > SQL Server > Restart > OK.
   5.  Navigate to System > Batch process (MUST RUN ON SERVER 10.100.13.10)
   6.  Capture Screen & paste it on somewhere.
   7.  Opening day (stats: ONLINE and Current working date must be the next date)


### Go back to server 10.102.34.222

### Export report (WISE KLS) - (After EOD)

1. CP23
   - Navigate to MIS Report > Collection report > CP23
   - Click “Init ” and select criteria as below
   ```
   Branch : Head Office 
   To Date : Current Date
   ```
   - Accept
   - Export
   - Close

2. LC001 
   - Navigate to MIS Report > Collection report > LC001
   - Click “Init ” and select criteria as below
   ```
   Form Assignment Date : 1 year back
   To Assignment Date : Current Date 
   Branch : Head Officer
   ```
   - Accept
   - Export
   - Close
   
3. LN904
   - Navigate to MIS Report > Collection report > LN904
   - Click “Init ” and select criteria as below
   ```
   Branch : Head Office 
   To Date : Current Date 
   ```
   - Accept
   - Export
   - Close
   
4. LN803A
   - Navigate to MIS Report > Credit report > LN803A
   - Click “Init ” and select criteria as below
   ```
   Business : All
   From Date : 01/01/2023 - Current date
   To Date : Current Date 
   Loan Origination Status : All
   Brach : Head Office
   ```
   - Accept
   - Export
   - Close

5. LN156
   - Navigate to MIS Report > Credit report > LN156
   - Click “Init ” and select criteria as below
   ```
   To Date : Current Date 
   ```
   - Accept
   - Export
   - Close

6. LN803S
   - Navigate to MIS Report > Credit report > LN803S
   - Click “Init ” and select criteria as below
   ```
   Business: All
   From Date : 1 year back
   To date : Current Date 
   Loan Origination Status : All
   Branch : Head Officer
   ```
   - Accept
   - Export
   - Close
  
7. LN805A
   - Navigate to MIS Report > Collection report > LN805A
   - Click “Init ” and select criteria as below
   ```
   Business: All
   Form Assignment Date : 01/01/2024 - Current Date
   To Assignment Date : Current Date 
   Branch : Head Officer
   ```
   - Accept
   - Export
   - Close



### Copy File
>C:\client_pro\EXCELOUTPUT\ "FILE NAME" TO C:\Daily report_KLS
```bash
1. 000435_LN051T_2039.txt
2. 000435_LN803_2046.XLS

3. 000435_CP23_2030.XLS
4. 000435_LC0001_2156.XSL
5. 000435_LN904_2202.XSL
 
6. 000435_LN803S_2046.XLS
7. 000435_LN805A_2027.XSL
8. 000435_LN803A_2139.XLS 
9. 000435_LN156_2202.XSL
```

### Save file 

>C:\Daily Report => Open LN803 File => save as excel file (.xlsx) => Sale_Dashboard folder => KLS_LN803
>
>C:\ifrs > Open LN904_KLS => save as excel file (.xlsx) => Import_data_Collection Platform => LN904_KLS

### Remote to Server : 10.100.13.10
   - Go to D:\wfbackup Move file WFWH to D:\wfbackup_WH, 
   - keep only WFBDS and WFHOST on folder wfbackup

### Restart SQL 
   1.  Restart Service SQL Server
   2.  Service => SQL Server => Restart => OK.
   3.  Task schedule => running > command Run > OK


```
```

# EOM => List of reports to generate after run batch on EOD

```
1.	LN803P and LN803B (KLS and KSM) – For BD 
-	Select end of month
-	After generate copy report to share drive =>Diary report =>manual =>LN803P and LN803B
-	Done
```
```
2.	LN804B (KLS and KSM) – For BD
-	Select end of month
-	After generate copy to drive =>Diary report =>manual =>LN804B
```

#### 3.	LN801 (KLS) – For Risk

>-	Open excel file LN801 in Drive D on server 10.102.34.29
>	
>- This Pc =>New Volume(D:) =>LN801 =>LN801 as of 30.04.2024_2
```
-	Go to query tab
-	Go to edit
-	Edit query change the date to end of month
-	Close and load
-	After finished copy file to =>Diary report =>manual =>LN801
```
```
4.	LN111 (KSM) – For Risk
-	Generate in wise
-	Select end of month
-	After finished copy file to =>Diary report =>manual =>LN111
```
### ກ່ອນລັນ EOD
```
5.	LN051A (generate before EOD only KLS) – For Finance
-	Select end of month
-	After done send email to Finance team with report
```

## Report Error

>- remote server 10 => Component Server => right click icon WBReports => select Shut down


