# KSM

## Remote desktop to 10.102.34.29
```bash
.\wiseksm
Wi$e@dm1n
```
### Run Batch
   1.  Navigate to System > Batch process (MUST RUN ON SERVER 10.102.34.29)
   2.  Opening day (stats: ONLINE and Current working date must be the next date)

### Export report (After EOD)

1. LN051T
   - Navigate to MIS Report > General ledger report > LN051T
   - Click “Init ” and select criteria as below
   ```
   Branch : Head Office
   To Date : Current Date 
   Business : All
   Product : All
   Port Transfer : All.
   ```
   - Accept
   - Export
   - Close

2. LN803A
   - Navigate to MIS Report > Credit report > LN803A
   - Click “Init ” and select criteria as below
   ```
   Business : Leave Blank
   Form Date : 1 year Back
   To Date : Current Date 
   Loan Origination Status : All
   Branch : Head Office
   ```
   - Accept
   - Export
   - Close

 3. LN803
    - Navigate to MIS Report > Credit report > LN803
    - Click “Init ” and select criteria as below
    ```
    Business : Leave Blank
    Form Date : 01/10/2022 - Current date
    To Date : Current Date 
    Loan Origination Status : All
    Branch : Head Office
    ```
    - Accept
    - Export
    - Close

4. LN156
   - Navigate to MIS Report > Credit report > LN156
   - Click “Init ” and select criteria as below
   ```
   To Date : Current Date 
   ```
   - Accept
   - Export
   - Close
     
5. CP23
   - Navigate to MIS Report > Collection report > CP23
   - Click “Init ” and select criteria as below
   ```
   Branch : Head Office 
   To Date : Current Date
   ```
   - Accept
   - Export
   - Close
     
6. LN904
   - Navigate to MIS Report > Collection report > LN904
   - Click “Init ” and select criteria as below
   ```
   Branch : Head Officer
   To Date : Current Date
   ```
   - Accept
   - Export
   - Close

7. LC001
   - Navigate to MIS Report > Collection report > LC001
   - Click “Init ” and select criteria as below
   ```
   From Assignment Date : 1 Year Back
   To Assignment Date : Current Date 
   Branch : Head Officer
   ```
   - Accept
   - Export
   - Close

### Copy File
>D:\client TO C:\ifrs
   ```
   000435_CP23_2030.XLS
   000435_LN051T_2039.txt
   000435_LC0001_2156.XSL
   000435_LN904_2202.XSL
   00435_LN803A_2139.XLS
   00435_LN803_2046.XLS
   00435_LN156_2139.XLS
   ```
### Save file 
>C> ifrs > Open LN803 File > save as excel file (.xlsx) > Sale_Dashboard folder
>C> BPW_Reprot > Open LN904 File > save as excel file (.xlsx) > Import_data_Collection Platform > folder LN904_KSM
