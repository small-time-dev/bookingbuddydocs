# Welcome!!!

This page contains information, instructions and formatting standards for Booking Buddy.

- [Readme First!](#readme-first)
- [What has changed in Version 2?](#what-has-changed-in-version-2)
- [Formatting Standards](#formatting-standards)
- [Instructions](#instructions)
- [Before starting](#before-starting)
- [Adding bookings](#adding-bookings)
- [Creating one-off and recurring bookings](#creating-one-off-and-recurring-bookings)
- [Before updating sheets](#before-updating-sheets)
- [Updating sheets](#updating-sheets)
- [Errors](#errors)




# Readme First!
Booking Buddy manages our Participants bookings.

Booking Buddy can:
1. Transform bookings from Google forms into individual rows (see "Raw data" tab)
2. Create one-off and recurring bookings (see "Create Bookings" tab)
3. Sort by date and name (see "All bookings" tab)
4. Retrieve all bookings for a given Participant (see "Search results" tab)
5. Create and/or update a given Participants Booking Buddy.
6. Sends an automated update email from you to the Participant.
7. Provide the link to a Participants Booking Buddy (see "All bookings" tab, column L)
8. Update all client booking buddy's at once ("All bookings")


Sheet Tabs:
1. All bookings
2. Search results
3. Sheet ID Keys (hidden)
4. Create Bookings
5. Raw data


#
### Caution 
***Sheet ID Keys*** is hidden because it is ***crucial*** for creating and updating each Participants sheet. 
Changes to this sheet will create issues.
If you need to find a Participants Email or a Participant appears to have multiple Booking Buddy's (***spaces*** were present in Clients name etc), you can investigate here. 
Please use caution when accessing this sheet.




#
## What has changed in Version 2?
1. Update all sheets button

2. Date for a given booking is now only handled in one column (B). This speeds up sorting, transforming and sheet updating.

3. Booking Buddy update and creation now use Participant Name (not Email). This allows families with multiple Participants to have a Booking Buddy for each child.

4. Removed columns: "PUDO Wanted?", "Info for sheet" & "Information added during booking (not copied to booking sheet)" from Booking Buddy, and "Additional Information" from individual client sheets.

5. The link for a clients sheet is now a descriptive hyperlink, e.g. "Click this link for John Johnson's Booking Buddy".

#
## Formatting Standards
Booking Buddy is built on top of Google Sheet. Due to this, we have to keep in mind a few things to use it properly.
### Spaces
***Spaces*** (also known as whitespace) matter... a lot!
Clients names should not have ***spaces*** before or after their name.


### Pick up & Drop off times
Enter times in 24 hour format as 00:00
For example: 06:00, 10:00, 13:00, 21:00.
Make sure there are no ***spaces*** before or after the time.
The cell will automatically format itself.
Column I & J (in "All bookings" and "Search results") display the format "8:45 am" but must be entered as in 24 hour format "08:45".
PUDO = Pick up & Drop off


### Matching bookings
For the spreadsheet to work correctly, each booking must have the correct email attached to it. Make sure there is no ***spaces*** before or after the email!

### Accidents
Accidentally clicking and dragging certain cells (resulting in the cell being moved) can cause further problems. If you run into a problem like this, pressing Undo (Command Z on Mac, Ctrl Z on Windows).

### Quirk
The "Retrieve & Save bookings" button will search for the "All bookings" tab and will update each matched bookings. This means that all of a given Participants bookings in "Search results" will overwrite the same bookings in "All bookings"

### Helpful tip
To select Participants Names easier in "Search results" (row 3 column C->E), sorting the "All bookings" by Date in the "All bookings" tab will make the list alphabetical.






#
#
# Instructions
#
# Before starting
1. Check if anyone is currently using the sheet and if they are, communicate with them to make sure you aren't interfering with their work. You will see a circle containing a letter in the top right. Click it and it will take you to where they are in the sheet!


2. Go to "Search results", select the drop down (row 3 column C->E) and select "empty" (you can also type to find it).

3. Click Retrieve & Save bookings (this will stop duplication errors or overwriting your current work)

#
#
# Adding bookings
### A note regarding raw booking format standard
Certain characters can cause problems. 
This standard should already be adhered to when each Google form is created, though, it is still important to check the bookings before transforming them.
#### Format Standard
A given day to book should be entered into the form like so:
"Monday 18th December - Ninja Parc Soft Play and Warrior Corse & Blaxland Riverside Park ($20)".

A cell can contain multiple bookings, for example: "Tuesday 26th September - Bounce Inc. Homebush ($23), Thursday 28th September - Shine Shed ($16), Saturday 30th September - Art Gallery NSW ($5)"

The "-" Symbol is used to separate the date and the activity; Date: "Monday 18th December", Activity: "Ninja Parc Soft Play and Warrior Corse & Blaxland Riverside Park ($20)".

Do not use the "-" inside of an activity. Instead, use & or @ or anything else.
This quirk is due to how Booking Buddy is built, and solving this problem in code appears to cause more problems than it solves.

#
## Bookings from Google forms
1. Go to the "Raw data" tab

2. Enter the participants email, name, and bookings on the next available row (@ or after row 7). 

Check that there is no additional ***spaces*** before are after the participants name or email. ***This is very important***.

3. Once ready, click the "Prepare bookings" button.
These newly transformed bookings will appear at the bottom at the bottom of the list of bookings in "All bookings". 

4. It is best practice to check that all the bookings have been added, check each row against the bookings listed in the relevant Google form.

5. Next, Add the Booking Time (column E), e.g. "9 am to 3 pm". This format is not strict, but looks nice.

6. Lastly, make sure each booking has the correct clients email in the final column (L)


#
## Adding bookings directly:
1. Go to the "All bookings" tab
Only add new bookings to "All bookings". Don't add new bookings to "Search results".

2. Enter the Participants' name in column A, ensuring their name is an identical match with their name in "All bookings", or "Sheet ID Keys" if no bookings present.

3. Enter the Participants' email in column L, again ensuring their email is an identical match with their email in "All bookings", or "Sheet ID Keys" if no bookings present.

4. Enter the date in column B (format DD/MM/YYYY, e.g. 16/12/2023)

5. Column C & D refer to column B, you can enter this formula =INDIRECT("B" & ROW()) or copy C & D from a row above and paste them into this row.

6. Now complete columns E, F, G, I, J and K as needed.


#
## Creating one-off and recurring bookings:
*** To create a one-off or recurring booking, a Participant must already have a Booking Buddy.***

1. Go to the "Create Bookings" tab

2. Begin typing the Participants name in column A and select the correct name.

3. Type the date of the first shift (format DD/MM/YY 14/05/23) into column B

4. Type the booking time in column C (e.g. 3 pm to 7 pm)

5. Select the Booking Type in column D.

6. Add the Program or Staff name. This will be displayed as "Booking Type - Program/Staff Name", e.g. "Saturday Program - Ryde Aquatic Centre"

7. Select the frequency, then type in the number of bookings to create.

8. Click the "Create bookings" button



### Note: Create bookings sheet
To use this sheet to create a booking for a participant, they must already have a booking buddy.
Using this sheet to create a booking matches the participants name with their email and avoids errors. It also allows you to create repeating bookings at the given interval.




#
#
# Before updating sheets
## Clean & prepare bookings
1. Go to the "All bookings" tab

2. Sort by date

3. For each given program day, make sure the value in "Activity & Cost" (column F) is correct in each related row. 
Be aware that many types of bookings can occur on each given day (1:1's + School Holiday Program etc).

4. Do the same as above (point 2.) and ensure Booking Time (column E) is present and correct. 
Again, be aware of many types of bookings on a given day.

5. If working on group programs, update columns G -> K where relevant.

#
## Confirm/Waitlist
1. Click the check box on either Confirm or Waitlist (column G and H, respectively). 

Your selection will eventually appear in the Participants Booking Buddy. 

If you do not check either check box, the booking will not appear in the Participants Booking Buddy.

#
## Pick up & Drop off (PUDO)
1. If the Participant will have a Pick up or Drop off (PUDO), you must pay special attention to how you enter the time. 
PUDO timings are entered in column I and J.

2. PUDO timings ***must*** be entered in the format -> 00:00 (HH:MM). This is in 24 hour time (10:00 = 10 pm, 13:00 = 1 pm, 21:00 = 9 pm).

This format is ***strict***. Incorrect formatting can lead to further issues in Booking Buddy.




#
# Updating sheets
## A single sheet
1. Go to "Search results"

2. Select the drop down (row 3 column C->E) and select the Participant of interest (you can also type to find it).

3. Click the "Retrieve & Save bookings" button

4. Make the relevant changes

5. When ready, click the "Update this clients booking sheet" button

6. It is best practice to open the clients booking sheet (column F cell 4) to make sure the the bookings have been added and formatted correctly.

This process takes approximately 10 seconds.

*How it works*: Updates the changes from Search results onto All bookings, gets the clients bookings from All Bookings, gets the clients sheetID (or creates a new one if not found), in clients booking buddy sheet: unhides all rows, removes "Week: " rows, removes row borders, add new bookings, at top and bottom border, add formula to last column, adds "Week: " rows, hides PUDO columns (if empty), hides previous bookings, deletes a number of extra rows from bottom of sheet

#
## All sheets
***As this updates all sheets, review all bookings to avoid errors***
1. Go to "All bookings"

2. Make changes where needed

3. Check all of the bookings on this page, pay attention for changes in format or missing information.

4. Click "Update all Booking Buddy's.

This may take approximately 10-20 seconds per participant

*How it works*: Gets a list of names for each person in the "All bookings" sheet. Then it set timers and periodically checks the timers to see if it will be able to complete the process, if it won't finish then it will set a trigger and remember where to start from after 2 minutes. The individual sheet updating is the same as [A single sheet](#a-single-sheet)




#
## Errors
If you encounter an error, please email curtis@careculture.com.au with the subject: Booking Buddy Error

In the body, describe what the error said, what you are doing and what you did in the sheet before the error (e.g. copied information, attempting to update John Johnson Booking Buddy) and any other information that may be relevant.