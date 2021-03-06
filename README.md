# TGSessionsChecker

TGSessionsChecker is a tool that contains functionality to check the validity of telegram user session files (.session)

## How to use?

**1. Clone this repo.**

    git clone https://github.com/glebfel/TGSessionsChecker.git

**2. Add your own telegram credentials (*api_id* and *api_hash*) to *credentials.py* file.**

How to get your own *api_id* and *api_hash*? Follow the next steps:

    1. Login to your Telegram account (https://my.telegram.org/auth) with the phone number of the developer account to use.

    2. Click under API Development tools.

    3. A Create new application window will appear. Fill in your application details. There is no need to enter any URL, and only the first two fields (App title and Short name) can currently be changed later.

    4. Click on Create application at the end. Remember that your API hash is secret and Telegram won’t let you revoke it. Don’t post it anywhere!
    
   ◾  *Also, you can add proxy to use in validation process (it is recommended to use proxy from the same region as session accounts are) or you can simply left the string empty.*
   
After getting telegram api credentials:
   
    Add api_id and api_hash that you got to the API_ID and API_HASH varibles respectively in credentials.py file.

**3. Install all required dependencies from *requirements.txt* file.**

Using pip :

    pip install -r requirements.txt
    
**4. Create */sessions* folder in the project directory root and add all session files you want to check.**   

![Безымянный1](https://user-images.githubusercontent.com/65199250/178754000-e92df72e-ece6-43fe-9735-143b36de4e95.png)

**5. Run run.py and follow instructions from the console if needed.**

**6. After successful run: */valid_sessions* folder and *report.json* will be created:**

    ◾ /valid_sessions folder contains all session files which pass validation process.
      
    ◾ report.json contains all process logs: session name + reason of success or denial in validation process.
 
**Example of report file:**
    
![Безымянный](https://user-images.githubusercontent.com/65199250/178754676-4ddf7c5e-d388-489a-8f3f-c29efb753f0d.png)

***Warning!***

***Don't foget to clean /sessions folder if you want to add new sessions for validation.***
