## BRAINSTORM

### Main Page:
- DePauw University webpage.
- Sign up.
- Log in.

### Users:
1. ***Students***
- Sign up:
    - Name
    - DOB
    - DePauw email
    - Phone Number
    - Student ID
    - Gender
    - **user name**
    - **password**
- Log in:
    - user name
    - password
- User portal:
    - Bicycle Rental (1)
    - Car Sharing (2)
    - Student Driver (3)
    - Local Driver (4)
    - Summary of Local Transit (5)

2. ***Local Drivers***

### (1) Bicycle Rental Portal
1. Previous (for past rental).
2. Current (for current rental bicycle).
3. Future (for scheduled pick up).
4. Schedule a bicycle:
- Rent Now:
    - Required information:
        - Desired Return Time (could not be more than 24 hours from current time).
            - Check with all current and future rental of this student: no overlapping time of rental is allowed.
    - Show a List of Available Bicycles with information for each bicycle:
        - ID Number.
        - Pick up and Return Location (CDI, Union Building). 
- Schedule in advance:
    - Required information:
        - Desired Pick Up Time.
        - Desired Return Time (could not be more than 24 hours from current time).
            - Check with all current and future rental of this student: no overlapping time of rental is allowed.
    - Show a List of Available Bicycles with information for each bicycle:
        - ID Number.
        - Pick up and Return Location (East College, UB). 
- After Picking Bicycle (Show):
    - Bicycle ID.
    - Returned Time + Warning: $20 will be charged to students account for every 30 minutes delay in return.
    - Return Location.
    - Show this rental in student's rental portal (current/future).
- After Returning Bicycle (Show):
    - Remove this rental in `Current`.
    - Show this rental in `Previous`.

**DataBase Table**



    