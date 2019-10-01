# Connectivity Checker

Got this one from [this article](https://realpython.com/intermediate-python-project-ideas/).

## Technical Details

The main objective of this project is to check the status of sites. So, you need to write code for checking the status of a website.

You can choose to use either TCP or ICMP for your connections. The socket module is one to check out. You can also read Socket Programming in Python (Guide).

Through your chosen framework, be it the docopt, click, or argparse framework, you can add commands to allow users to add and remove sites from the list of sites to be checked.

The users should also be able to start the tool, stop it, and determine the intervals.

Since you’ll have to save the list of files to be checked, you can either save it in a file (just a list of sites) or use a SQLite database through the sqlite3 module.

### Extra Challenge

The application can check for the connectivity status of sites and display the results to the command-line. But this will require the user to keep checking the command-line.

You can increase the challenge and implement a notification feature. The notification feature can be a sound played in the background to alert the user when a site’s status changes. You’ll need a database to store the previous status of a site. That’s the only way the tool can tell when the status changes.