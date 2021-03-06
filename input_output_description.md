# Input/Output Description
- Input: A **zip file** with the following comma separated csv files. Reference file: sample.zip
- Details for each csv file:
    - cust.csv (required)
        - Required columns: 
            - cust_id: unique id for cust
            - area: location area
            - gender: gender
            - birth_dt: birth date
        - Optional columns (not used in model): 
            - education_level: education level
            - marriage_status: marriage status
            - yearly_income: annual income
    - card.csv (required)
        - Required columns: 
            - cust_id: unique id for cust
            - card_id: unique id for card
            - acct_id: unique id for account
            - open_dt: card open date
            - card_level: card level
            - cash_limit_amt: cash limit
            - curr_limit_amt: current limit

    - transaction.csv (required)
        - Required columns: 
            - card_id: unique id for card
            - purchase_amount: customer purchase amount
            - business_category: business category code
            - purchase_date: customer purchase date
    - app_data.csv (required)
        - Required columns: 
            - cust_id: unique id for cust
            - app_logon_date: customer logon app date
            - app_function: app function module
    - Note: if end user do not have optional tables, empty CSV with identical columns should be generated to replace missing optional table.
- Output: A list of JSON objects containing 'cust_id' and 17 columns added named 'score_category_i' which contains model's prediction of the recommendation likelihood score for the record for certain category i. Reference file: sample.zip.out
