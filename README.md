Version: 1.0.0
Author: [boredpydev]

##  **Program Overview**

This program automates the management of Stremio accounts and addons by dynamically logging into multiple accounts, removing non-default addons, and installing custom addons specified in a JSON configuration file. It also dynamically detects and preserves any Trakt-based addons, even if their IDs vary across accounts.

The script operates asynchronously, enabling it to process multiple accounts simultaneously for faster execution. It uses CSV files to store account credentials and authentication tokens, ensuring that subsequent runs reuse stored tokens whenever possible, only logging in again if a token is invalid or expired.

## **CSV Structure**
The program expects a CSV file named stremio_logins.csv with the following columns. The program generates the auth_token so leave field empty. 

`email,password,auth_token`



## Custom Addons and JSON Configuration
Custom addons are defined in a separate file called custom_addons.json. If the file does not exist, the program prompts the user to enter addon transport URLs in a loop until they type 'done'.

For each URL, the program fetches the manifest and flags directly from the addon source, ensuring accurate metadata. These addons are then saved in the JSON file and automatically installed to all accounts during execution.


> *If I have saved you time, consider donating **SOL**, thankyou & merry christmas. *

### 4dXf9Pnjjon2aA7bxoyJ1f8Y1Y1KmyThwxApj4XezHPY
