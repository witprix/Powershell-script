# Powershell-script
To Track my day to day info of it


The PowerShell Prompt
Open your platform-tools-latest-windows folder, hold Shift and Right-click in an empty space, then select "Open PowerShell window here." Copy and paste the following command:

PowerShell
.\adb.exe shell content query --uri content://sms/ > all_sms.txt
How to read the data
Once the command finishes, a file named all_sms.txt will appear in your folder.

Format: The data is exported as "key=value" pairs (e.g., address=5551234, body=Hello!).

Standard Columns:

address: The phone number.

body: The message content.

date: The timestamp (in milliseconds).

type: 1 for received (Inbox), 2 for sent (Sent).

Refining the Output
If the raw file is too messy and you only want the phone number and the message text, use this refined prompt:

PowerShell
.\adb.exe shell content query --uri content://sms/ --projection address:body
