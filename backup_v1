import os
import time

# Files and directories to be copied are collected in a list
dir_source = [
    "D:\\BOOKS\Social",
    "C:\\Users\Lucy.Corris\Desktop\python",
]
# Note that for names containing spaces, you must use
# double quotes inside the string.

# Backups must be stored in the primary reserve directory.
dir_sav = "D:\\Backup"  # Substitute the path that you will use.

# Files are placed in a zip archive.
# The name for the zip archive is the current date and time.
today = dir_sav + os.sep + time.strftime("%Y%m%d")
# The current time is the name of the zip archive
now = time.strftime("%H%M%S")

# Request user comment for file name
comment = input("Please input your comment --> ")
if len(comment) == 0:  # check if a comment is entered
    dir_done = today + os.sep + now + ".zip"
else:  # the reverse '\' if the line continues. on the next line
    dir_done = today + os.sep + now + "_" + comment.replace(" ", "_") + ".zip"

# Create a directory if it is not already
if not os.path.exists(today):
    os.mkdir(today)
print("Folder - created", today)

# Use the "zip" command to place files in a zip archive
zip_order = "zip -qr {0} {1}".format(dir_done, " ".join(dir_source))
# Run backup
if os.system(zip_order) == 0:
    print("The backup was successfully created in", dir_done)
else:
    print("Backing up FAILED")
