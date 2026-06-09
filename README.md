OrangeHRM 100 Comprehensive Test Cases Suite
This repository contains a professional, structured, and comprehensive suite of 100 test cases for the OrangeHRM (Open Source HR Management) platform. It covers all core modules with formal test case elements including Pre-conditions, Test Steps, and Expected Results.
📄 Test Cases Index by Module
Login & Authentication Module (TC-001 to TC-010)
Admin & User Management Module (TC-011 to TC-025)
PIM (Personnel Information Management) Module (TC-026 to TC-045)
Leave Management Module (TC-046 to TC-065)
Time & Attendance Module (TC-066 to TC-080)
Recruitment Module (TC-081 to TC-090)
Performance & Dashboard Module (TC-091 to TC-100)
1. Login & Authentication Module
TC-001: Verify login with valid Admin credentials
Pre-conditions: User is on the OrangeHRM Login Page. Valid admin credentials exist in the system.
Test Steps:
Enter valid admin username in the 'Username' field.
Enter valid admin password in the 'Password' field.
Click on the 'Login' button.
Expected Result: User should be successfully authenticated and redirected to the OrangeHRM Dashboard page.
TC-002: Verify login with invalid username and valid password
Pre-conditions: User is on the OrangeHRM Login Page.
Test Steps:
Enter an invalid/non-existent username in the 'Username' field.
Enter a valid password in the 'Password' field.
Click on the 'Login' button.
Expected Result: Login should fail. An error message "Invalid credentials" should be displayed on the screen.
TC-003: Verify login with valid username and invalid password
Pre-conditions: User is on the OrangeHRM Login Page.
Test Steps:
Enter a valid username in the 'Username' field.
Enter an invalid password in the 'Password' field.
Click on the 'Login' button.
Expected Result: Login should fail. An error message "Invalid credentials" should be displayed.
TC-004: Verify login with blank username and blank password fields
Pre-conditions: User is on the OrangeHRM Login Page.
Test Steps:
Leave the 'Username' field empty.
Leave the 'Password' field empty.
Click on the 'Login' button.
Expected Result: Inline validation messages saying "Required" should appear below both the Username and Password fields.
TC-005: Verify 'Forgot Your Password?' link functionality
Pre-conditions: User is on the OrangeHRM Login Page.
Test Steps:
Click on the 'Forgot your password?' link.
Expected Result: User should be redirected to the "Reset Password" page where they are asked to input their username.
TC-006: Verify password masking
Pre-conditions: User is on the OrangeHRM Login Page.
Test Steps:
Type characters into the 'Password' field.
Expected Result: The entered password characters should be masked and displayed as dots (•) or asterisks (*) for security.
TC-007: Verify session timeout after a period of inactivity
Pre-conditions: User is successfully logged into the system.
Test Steps:
Keep the browser session idle without performing any action for the configured timeout duration.
Try to click on any menu item after the timeout period.
Expected Result: The system should automatically log out the user and redirect them to the Login page with a session expired message.
TC-008: Verify 'Logout' button functionality
Pre-conditions: User is logged in and on the Dashboard page.
Test Steps:
Click on the user profile dropdown on the top right corner.
Click on the 'Logout' link.
Expected Result: User should be safely logged out, session token should be cleared, and redirected back to the login page.
TC-009: Verify login page responsiveness on different screen sizes
Pre-conditions: Tester has access to browser developer tools or multiple devices.
Test Steps:
Open the OrangeHRM login page on Mobile (375x812), Tablet (768x1024), and Desktop (1920x1080) dimensions.
Expected Result: All UI components (fields, buttons, logos) should adjust dynamically without overlapping or breaking layout alignment.
TC-010: Verify that pressing 'Enter' key triggers the login action
Pre-conditions: User is on the OrangeHRM Login Page.
Test Steps:
Enter valid credentials in the Username and Password fields.
Press the 'Enter' key on the keyboard.
Expected Result: The login action should trigger exactly like clicking the 'Login' button, and user should access the Dashboard.
2. Admin & User Management Module
TC-011: Verify adding a new System User with Admin role
Pre-conditions: User is logged in as an Admin and is on the Admin -> User Management -> Users page.
Test Steps:
Click on the '+ Add' button.
Select 'Admin' from the User Role dropdown.
Enter an existing Employee Name, choose a unique Username, Status as 'Enabled'.
Fill the password fields and click 'Save'.
Expected Result: The system user should be saved successfully and should be visible in the user management system list.
TC-012: Verify adding a new System User with ESS role
Pre-conditions: User is logged in as Admin, on the 'Add User' page.
Test Steps:
Select 'ESS' (Employee Self Service) from the User Role dropdown.
Fill all other mandatory fields (Employee Name, unique Username, Status, Password).
Click 'Save'.
Expected Result: User should be saved with ESS role access limitations.
TC-013: Verify searching for a user by Username
Pre-conditions: Admin is on the User Management list page. User records exist.
Test Steps:
Type a valid existing username in the 'Username' field of the search widget.
Click on the 'Search' button.
Expected Result: The grid view should filter and display only the record matching the typed username.
TC-014: Verify searching for a user by User Role
Pre-conditions: Admin is on the User Management list page.
Test Steps:
Select 'Admin' from the User Role search dropdown.
Click on the 'Search' button.
Expected Result: The system should filter and return all system records configured under the 'Admin' role.
TC-015: Verify searching for a user by Employee Name
Pre-conditions: Admin is on the User Management list page.
Test Steps:
Type an employee name in the predictive auto-suggest 'Employee Name' search field.
Select the specific employee from the auto-suggested list.
Click on the 'Search' button.
Expected Result: System returns user records associated with that specific employee name.
TC-016: Verify searching for a user by Status
Pre-conditions: Admin is on the User Management page.
Test Steps:
Select 'Disabled' from the Status dropdown field.
Click on the 'Search' button.
Expected Result: Only the system users whose status is set to 'Disabled' should appear in the results table.
TC-017: Verify that duplicate usernames cannot be created
Pre-conditions: Admin is on the 'Add User' page. An existing username "john.doe" exists.
Test Steps:
Enter "john.doe" in the Username field.
Move focus away from the field or fill other details.
Expected Result: System should instantly display a red validation message "Already exists" near the username text box.
TC-018: Verify editing an existing user's role or status
Pre-conditions: Admin is on the User Management list page.
Test Steps:
Find an existing user and click on their edit (Pencil) icon.
Change the Status from 'Enabled' to 'Disabled'.
Click on the 'Save' button.
Expected Result: The user details should update successfully and show the 'Disabled' status status indicator in the user grid.
TC-019: Verify deleting a single system user
Pre-conditions: Admin is on the User Management screen.
Test Steps:
Locate a system user record and click on its corresponding trash/delete icon.
Click 'Yes, Delete' on the confirmation pop-up alert dialog.
Expected Result: The user record should get deleted from the database and disappear from the user table list.
TC-020: Verify deleting multiple users using the checkbox selection (Bulk Delete)
Pre-conditions: Multiple system user records exist.
Test Steps:
Select checkboxes adjacent to multiple user rows.
Click on the 'Delete Selected' button located above or below the grid header.
Confirm the action in the pop-up modal.
Expected Result: All chosen user records must be purged together simultaneously.
TC-021: Verify validation message when leaving mandatory fields blank in 'Add User'
Pre-conditions: Admin is on the 'Add User' screen.
Test Steps:
Keep all fields clear and directly click on the 'Save' button.
Expected Result: Forms must not submit. Error messages saying "Required" should render beside all mandatory input boxes.
TC-022: Verify disabling a user account prevents them from logging in
Pre-conditions: A user account status has been changed to 'Disabled' by Admin.
Test Steps:
Navigate to the login screen.
Fill credentials of that disabled user account.
Click 'Login'.
Expected Result: Authentication fails, account access block notice or message should appear.
TC-023: Verify password strength validation while creating a new user
Pre-conditions: Admin is on 'Add User' page.
Test Steps:
Input a weak single-case password like "123" in the password field.
Expected Result: System prompt message should appear indicating password criteria is unmet (e.g., must contain minimum characters, symbols, numbers).
TC-024: Verify 'Reset' button functionality in User Search bar
Pre-conditions: Admin filled search inputs (Username, Status fields).
Test Steps:
Click on the 'Reset' button adjacent to search parameters.
Expected Result: All custom search input parameters should instantly clear out, reverting the data table list view to show default records.
TC-025: Verify pagination on the User Management screen
Pre-conditions: Total user system database records count exceeds 50.
Test Steps:
Scroll down to the bottom of the active user list window.
Click on page navigation element number '2' or 'Next' arrow control icon.
Expected Result: System should successfully render the following subset batch of system users smoothly.
3. PIM (Personnel Information Management) Module
TC-026: Verify adding a new employee with only mandatory fields
Pre-conditions: Logged in as Admin/PIM manager. Navigated to PIM -> Add Employee.
Test Steps:
Fill out 'First Name' and 'Last Name' input fields.
Leave other fields completely empty.
Click on the 'Save' button.
Expected Result: Employee profile record gets created and the UI redirects to the Personal Details edit interface view.
TC-027: Verify adding a new employee with an optional photograph
Pre-conditions: PIM -> Add Employee screen open. A valid graphic file (.jpg/.png) is prepared.
Test Steps:
Input First and Last name.
Click on the Profile Image attachment container icon.
Select and upload the file. Click 'Save'.
Expected Result: Profile saves correctly and shows the uploaded picture layout successfully.
TC-028: Verify 'Create Login Details' checkbox functionality while adding an employee
Pre-conditions: User is on the PIM Add Employee form window interface.
Test Steps:
Toggle/check the 'Create Login Details' switch component checkbox.
Expected Result: Expanded sub-form fields for Username, Password, Confirm Password, Status should dynamically become visible.
TC-029: Verify searching an employee by Name/ID in Employee List
Pre-conditions: User is on PIM -> Employee List page view.
Test Steps:
Enter a valid pre-existing Employee Name or specific ID code into the designated search bar textbox field.
Press the 'Search' action icon button element.
Expected Result: Data table row updates filtering exclusively matching query string data rows.
TC-030: Verify searching an employee by Employment Status
Pre-conditions: Employee List configuration contains records with diverse employment classes.
Test Steps:
Under search parameters panel, pick 'Full-Time Permanent' from employment status dropdown field selection list.
Click 'Search'.
Expected Result: Grid updates displaying data records matched to that specified Employment Status parameter constraint.
TC-031: Verify searching an employee by Job Title
Pre-conditions: Employee list screen is accessible.
Test Steps:
Select a designated job role label option (e.g., "QA Engineer") out from the Job Title select field component.
Execute 'Search'.
Expected Result: The filtered array yields records mapping to the assigned designated Job Title criteria index.
TC-032: Verify searching an employee by Sub Unit (Department)
Pre-conditions: Corporate organizational multi-tier departments structured setup completed.
Test Steps:
Pick 'Development' department identifier item from Sub Unit filter selection selector.
Click 'Search'.
Expected Result: Search query filters list showing profiles grouped precisely under the respective targeted organizational subunit block.
TC-033: Verify updating an employee's Personal Details
Pre-conditions: Admin/HR is looking at an employee's specific dashboard sheet view layout.
Test Steps:
Select Personal Details sub-tab column block profile area.
Edit attributes: Marital Status string, Nationality option value, Date of Birth.
Hit 'Save'.
Expected Result: Profile registers changes. Success alert pops up confirmation notification text block.
TC-034: Verify updating an employee's Contact Details
Pre-conditions: Employee dashboard section is open.
Test Steps:
Click on Contact Details option.
Modify 'Street 1', 'Mobile Phone Number', and 'Work Email Address'.
Click 'Save'.
Expected Result: Operational database details map accurately without configuration drop loss errors.
TC-035: Verify adding Emergency Contacts for an employee
Pre-conditions: Emergency Contacts panel chosen on employee record sub-navigation page menu structure.
Test Steps:
Click '+ Add Assigned Emergency Contact'.
Input name identity value text, relationship mapping type, contact mobile string info.
Click 'Save'.
Expected Result: Contact gets appended table rows data array perfectly.
TC-036: Verify adding Dependents details for an employee
Pre-conditions: Dependents page layout open.
Test Steps:
Click on '+ Add' inside the Dependents data layout section widget.
Provide Full Name, Select Relationship mapping link type (Child/Spouse/Other), Date of Birth details string.
Save.
Expected Result: Household dependent parameters record establishes successfully under system profile mapping list.
TC-037: Verify updating Job Information
Pre-conditions: HR Manager has loaded target employee profile profile screen.
Test Steps:
Choose 'Job' information screen left-side panel view section option.
Modify Joining Date, select updated corporate Job Title tier level, modify job categorization code structure parameters.
Click 'Save'.
Expected Result: Internal system profiles configuration update records status historical job log entries tracker accurately.
TC-038: Verify assigning a Supervisor / Report-to manager
Pre-conditions: PIM menu profile configuration open.
Test Steps:
Go into the 'Report-to' section area subview panel.
Click '+ Add Supervisor'.
Query name tag lookup select target management employee identity, specify reporting format type link logic option (Direct/Indirect).
Save.
Expected Result: Organization line structure binds profile reporting structure linking relationship cleanly.
TC-039: Verify uploading attachments in employee records
Pre-conditions: User viewing profile dashboard layout section.
Test Steps:
Scroll down to look at 'Attachments' management box tool.
Select '+ Add'. Select valid electronic archive documentation item file format (.pdf/.docx).
Click 'Upload'/'Save'.
Expected Result: Files upload to the system server layout structure repository securely, listed visually cleanly inside data tables.
TC-040: Verify deleting an employee record from PIM list
Pre-conditions: HR/Admin viewing full PIM system records employee overview registry table block.
Test Steps:
Check checkbox container row matching targeted test employee profile database entry row record.
Select the absolute row trash bin click trigger icon element.
Authorize popup verification dialog option.
Expected Result: Profile vanishes cleanly, dependencies mapped system links clear out properly.
TC-041: Verify automatic generation of Employee ID if left blank
Pre-conditions: Add Employee menu screen active.
Test Steps:
Clear standard prepopulated/empty data inside 'Employee ID' numeric/alphanumeric textbox field.
Input First & Last Name string tags. Click 'Save'.
Expected Result: profile saves perfectly. System creates automated serialized sequence identification index code value tagging item profile.
TC-042: Verify that duplicate Employee IDs are not allowed
Pre-conditions: Employee code index id "0077" exists in the operational backend registry records.
Test Steps:
Launch Add Employee workspace screen.
Force string override inputting "0077" inside 'Employee ID' parameter field.
Populate remaining mandatory properties text data elements. Attempt to click 'Save'.
Expected Result: Validation warning message "Employee ID already exists" highlights underneath specific index field text input.
TC-043: Verify Custom Fields functionality in PIM
Pre-conditions: Admin configured custom tracking parameter entity fields data (e.g., Blood Group Type).
Test Steps:
Access target employee record profile sheet overview.
Locate configuration block custom fields view section, modify custom drop selection values array box.
Click 'Save'.
Expected Result: Specific personalized data fields store and render cleanly without affecting core standard schema objects layout.
TC-044: Verify exporting employee list to a CSV/Excel file
Pre-conditions: User viewing comprehensive general Employee List grid data sheet layout view page dashboard.
Test Steps:
Locate and trigger action icon link button standard 'Export' tool choice option element icon.
Expected Result: System processes requests, browser initiates download sequence producing matching structured tabular electronic document format text data sheet (.csv/.xlsx).
TC-045: Verify that a deleted employee's login credentials become invalid immediately
Pre-conditions: Employee system record profile has just been fully purged via Admin PIM action ruleset.
Test Steps:
Log out of Admin account.
Access default user system entry gateway dashboard.
Fill input forms fields utilizing deleted profile user account login parameter keys values. Click 'Login'.
Expected Result: Gateway blocks entry completely, throwing standard unauthenticated access user verification block system notification error text flags.
4. Leave Management Module
TC-046: Verify defining/configuring a new Leave Type
Pre-conditions: Logged in as Admin/HR Leave Manager. Path: Leave -> Configure -> Leave Types.
Test Steps:
Click on the '+ Add' item link layout tool option element.
Enter field string values name label tag text block (e.g., "Maternity Leave").
Configure rule parameters switches logic choice check toggles. Click 'Save'.
Expected Result: Newly created configuration profile class option appends system select options.
TC-047: Verify Entitling leaves to a specific employee
Pre-conditions: Leave Type created, operational leave periods configured properly. Path: Leave -> Entitlements -> Add Entitlements.
Test Steps:
Choose individual configuration toggle mode 'An Employee'.
Query text auto-suggest lookup targeted operational worker tag label.
Choose 'Leave Type' object item, configure specific allocated total numerical allotment number (e.g., "15.00").
Click 'Save'.
Expected Result: Target employee profile tracking matrix balances update to register newly allocated credit unit quantities.
TC-048: Verify Entitling leaves to multiple employees (Bulk Entitlement)
Pre-conditions: Leave Management settings active.
Test Steps:
Select structural allocation radio item choice option 'Multiple Employees'.
Pick specific filter parameter properties structural unit tags: Sub Unit = "QA Team", Location = "HQ Office".
Pick specific Leave Type option index label string, feed target credit integers quantity.
Click 'Save' and confirm allocation dialog block popup prompt.
Expected Result: Every profile entity intersecting target tracking criteria metrics updates structural data matrix balances.
TC-049: Verify applying for a leave with sufficient leave balance
Pre-conditions: ESS profile logged in. Has remaining active credit balance of 10 days for 'Casual Leave'.
Test Steps:
Path: Leave -> Apply. Select Leave Type option item "Casual Leave".
Specify calendar schedule dates time length spanning 3 continuous calendar days.
Fill out comment placeholder area text block. Click 'Apply'.
Expected Result: Process submits successfully without exceptions, changing leave tracking status index state flag to 'Pending Approval'.
TC-050: Verify applying for a leave with insufficient leave balance
Pre-conditions: ESS profile account balance totals 2 available balance credit counting units.
Test Steps:
Select leave submission workspace option layout.
Pick target leave configuration category, request single block sequence stretch spanning 5 operational workflow days.
Expected Result: Screen shows warning alert flag "Balance Insufficient" text marker notification block, blocking request routing if rules prevent negative balance.
TC-051: Verify applying for a partial day / half-day leave
Pre-conditions: ESS user profile system menu interface dashboard layer active.
Test Steps:
Navigate configuration dropdown select option properties component tagged 'Duration'.
Switch properties toggle value mode selector choice to 'Half Day' or 'Specify Time'.
Pick specific timeline shift block target slot (e.g., "Morning Shift"). Click 'Apply'.
Expected Result: Request files accounting for fractional calculation value units (0.5 work unit factor metrics ratio scale).
TC-052: Verify Leave Calendar view for an employee
Pre-conditions: Leave records exist for the employee.
Test Steps:
Go to Leave -> My Leave List or Calendar view.
Expected Result: A graphical monthly/weekly calendar grid is displayed, with leave days highlighted in specific colors matching their status (Approved/Pending).
TC-053: Verify Admin/Manager can 'Approve' a pending leave request
Pre-conditions: Supervisor manager logged in. An employee has submitted a pending leave request.
Test Steps:
Navigate to Leave -> Leave List page overview.
Locate row entry containing employee's pending leave application.
Choose item action option button labeled 'Approve' from dropdown action choices grid column block. Click 'Save'.
Expected Result: Application updates lifecycle tracking parameters state flags to 'Scheduled/Approved' cleanly.
TC-054: Verify Admin/Manager can 'Reject' a pending leave request
Pre-conditions: Supervisor review list workspace layout tracking board active.
Test Steps:
Find specific targeted tracking row record mapping to employee's leave request.
Click action status option choice control selector element labeled 'Reject'.
Supply explanation details string context inside text notes comment dashboard box. Click 'Save'.
Expected Result: Request status state updates setting structural identifiers flag to 'Rejected' status value.
TC-055: Verify Admin/Manager can 'Cancel' an approved leave request
Pre-conditions: Target leave application has already transitioned into 'Approved' lifecycle stage state rules tracking index.
Test Steps:
Access active organizational tracking review records overview sheet data panel view.
Locate active upcoming approved schedule entry. Click structural selection action override tool option element marked 'Cancel'.
Expected Result: Leave item moves status identifier category assignment over to 'Cancelled', adjusting tracking credit integer ledger balances.
TC-056: Verify an employee can cancel their own pending leave request
Pre-conditions: ESS profile logged in. A leave request exists in 'Pending Approval' status.
Test Steps:
Navigate to Leave -> My Leave List.
Locate the pending leave request and click on its 'Cancel' action button.
Expected Result: The status changes to 'Cancelled' and the requested days are instantly freed up in the employee's active balance view.
TC-057: Verify Leave Comments functionality between employee and manager
Pre-conditions: An active leave request lifecycle is ongoing.
Test Steps:
As an employee, add a comment "Family emergency" during leave application.
As a manager reviewing the leave list, open the comment dialog box.
Expected Result: The manager can read the employee's comments, and any comment added by the manager is visible to the employee under their leave history list.
TC-058: Verify Leave Balance is deducted correctly after approval
Pre-conditions: Employee has 12 days balance. Applies for 3 days of leave.
Test Steps:
Manager approves the 3-day leave request.
Check the employee's Leave Entitlements and Usage page tracking.
Expected Result: The system should show: Entitled = 12, Taken = 3, Balance = 9 days.
TC-059: Verify overlapping leave requests are not allowed for the same dates
Pre-conditions: Employee has an approved leave from Oct 10 to Oct 12.
Test Steps:
Attempt to apply for another leave of any type for Oct 11 to Oct 14.
Expected Result: System validation should block the submission, displaying an error message "Leave application overlaps with an existing leave request".
TC-060: Verify configuring 'Holidays' in the leave calendar
Pre-conditions: Admin user logged in. Path: Leave -> Configure -> Holidays.
Test Steps:
Click '+ Add'. Enter Holiday Name (e.g., "New Year's Day").
Select Date and check the 'Full Day' or 'Half Day' checkbox. Click 'Save'.
Expected Result: The holiday is saved and reflected on the global corporate holiday calendar records list.
TC-061: Verify configured holidays are not counted as working days in leave application
Pre-conditions: Friday is configured as a global Holiday. Saturday and Sunday are default weekend days off.
Test Steps:
Apply for leave from Thursday to Monday (5 calendar days total).
Expected Result: The total leave days calculated by the system should equal 2 days (Thursday and Monday), automatically ignoring the Friday holiday and weekends.
TC-062: Verify viewing 'My Leave List' as an ESS user
Pre-conditions: Logged in as regular employee (ESS role).
Test Steps:
Navigate to Leave -> My Leave List from the main navigation sidebar panel.
Expected Result: The user sees only their personal leave applications, and cannot view other corporate employees' records.
TC-063: Verify viewing 'Leave List' as an Admin for all employees
Pre-conditions: Logged in as Admin user.
Test Steps:
Navigate to Leave -> Leave List. Leave search criteria fields broad/default and click 'Search'.
Expected Result: Detailed records of leave requests from all organizational employees are fetched and displayed in a central data grid layout.
TC-064: Verify Leave Period configuration
Pre-conditions: Admin logged in. Path: Leave -> Configure -> Leave Period.
Test Steps:
Observe or edit the start month and start day properties of the corporate tracking fiscal calendar year.
Expected Result: System enforces global tracking rules across entitlements based on the chosen leave period setting (e.g., Jan 01 – Dec 31).
TC-065: Verify automated email notification sent to manager upon leave submission
Pre-conditions: Email configuration setup correctly in Admin settings. Employee has a designated supervisor.
Test Steps:
Logged in as ESS user, submit a new leave application request.
Expected Result: An automated alert notification email is instantly delivered to the supervisor's mapped corporate inbox detailing the request parameters.
5. Time & Attendance Module
TC-066: Verify Punch In functionality with current time
Pre-conditions: User logged into ESS portal dashboard. Time tracking configuration enabled.
Test Steps:
Navigate to Time -> Attendance -> Punch In/Out.
Verify system clock displays accurate current localized timestamp. Click on the 'Punch In' button.
Expected Result: Status shifts seamlessly to clocked-in state, showing a green check indicator or a 'Punch Out' tracking action option interface button.
TC-067: Verify Punch Out functionality with current time
Pre-conditions: Employee is currently in a clocked-in status state inside the platform tracking session.
Test Steps:
Open Time attendance dashboard interface workspace.
Click on the active 'Punch Out' button element control link.
Expected Result: System registers checkout timestamp data entry record parameters, calculates running log intervals, and displays a successful checkout state screen message.
TC-068: Verify adding a note/comment during Punch In/Out
Pre-conditions: Attendance menu open.
Test Steps:
Type a message text string (e.g., "Working remotely from client office site location") inside the Note text field area container.
Click the 'Punch In' or 'Punch Out' action button component.
Expected Result: Note payload securely binds alongside corresponding timestamp transaction records table rows database matrix layer.
TC-069: Verify editing a punch-in time record
Pre-conditions: Admin role logged in, or configurations grant edit permissions rights parameters tools accessibility.
Test Steps:
Go to Time -> Attendance -> Employee Records.
Locate targeted attendance log record entry line item, select edit configuration tools element icon.
Modify timestamps clock digit properties. Click 'Save'.
Expected Result: Record updates cleanly, retaining a localized visual log tracker identifying manual override correction parameters.
TC-070: Verify viewing 'My Timesheet' for the current week
Pre-conditions: ESS profile logged in. Timesheet configuration settings initialized.
Test Steps:
Navigate layout options list framework path: Time -> Timesheets -> My Timesheets.
Expected Result: Grid structural workspace displays current running calendar block tracking columns divided across days layout matrix cleanly mapping logs.
TC-071: Verify submitting a Timesheet for approval
Pre-conditions: User entered hour values mapping tasks entries inside current timeline block tracking matrix sheets.
Test Steps:
Open active personal Timesheet summary panel workspace screen view.
Click on the 'Submit' button control element icon tool.
Expected Result: Current tracking sheet parameters status lock down completely from edits, changing state identifier flag context over to 'Submitted'.
TC-072: Verify Manager can Approve a submitted timesheet
Pre-conditions: Manager account logged in. A direct report employee has submitted their timesheet.
Test Steps:
Navigate to Time -> Timesheets -> Employee Timesheets.
Click on the pending timesheet row of the employee.
Review logs data and click on the 'Approve' action button control.
Expected Result: Timesheet tracking state updates to 'Approved', locking the data records completely against any changes.
TC-073: Verify Manager can Reject a submitted timesheet with feedback
Pre-conditions: Timesheet submission active in reporting review pipeline workspace tracking module.
Test Steps:
Open submitted employee timesheet sheet panel.
Click on 'Reject' button element.
Enter text comment: "Missing log details for Project X on Tuesday". Save.
Expected Result: Timesheet loops backwards reverting status flags configuration state to 'Rejected / Draft Mode', opening input fields to the employee again.
TC-074: Verify creating a new Project in Time module
Pre-conditions: Admin/Project Manager access permissions active. Path: Time -> Project Info -> Projects.
Test Steps:
Click on '+ Add'. Select/Input Customer name index label, type unique Name (e.g., "Mobile Banking App V2").
Assign a Project Admin user profile context. Click 'Save'.
Expected Result: Project item creates successfully, allowing management configuration dependencies association setup routines.
TC-075: Verify creating Project Customers
Pre-conditions: Time module workspace active.
Test Steps:
Path: Time -> Project Info -> Customers. Click '+ Add'.
Provide Customer Name value string and add description notes details block. Click 'Save'.
Expected Result: Customer account creates cleanly, listing inside selectable dropdown fields during new project creation maps.
TC-076: Verify assigning Project Activities to employees
Pre-conditions: Project record created. Project Details dashboard pane workspace active.
Test Steps:
Inside active Project Profile workspace layout screen pane, find 'Activities' subview. Click '+ Add'.
Type activity name (e.g., "UI Automation Testing"). Save configuration mapping link profiles.
Expected Result: Work activity labels map into project properties arrays, opening assignment tracking capability interfaces.
TC-077: Verify logging hours against specific project activities in timesheet
Pre-conditions: ESS profile has assigned task project tracking items mappings initialized.
Test Steps:
Open personal Timesheet workspace grid editor screen view.
Select row dropdown menu fields, match Customer -> Project -> Activity.
Input numeric tracking integer data inside day mapping column fields (e.g., Monday = "8"). Click 'Save'.
Expected Result: Running entry structures track values, calculating aggregate vertical summary row computations accurately.
TC-078: Verify validation for entering negative hours in timesheet
Pre-conditions: Timesheet editor screen active.
Test Steps:
Type a negative numeric metric string text value (e.g., "-4") inside a day time mapping field box block.
Click 'Save'.
Expected Result: UI blocks submission processing operations, raising error validation message indicators stating format value issues.
TC-079: Verify validation for entering more than 24 hours in a single day
Pre-conditions: Timesheet logging workspace grid screen layout active.
Test Steps:
Input numerical configuration tracking value integer "25" inside a single day log box column field container.
Click 'Save'.
Expected Result: Validation routine triggers check constraints, throwing error popups warning input exceeds absolute maximum daily real-time hour boundaries.
TC-080: Verify viewing Attendance Reports for a specific department
Pre-conditions: Admin/HR logged in. Attendance logging records exist across various corporate sections.
Test Steps:
Path: Time -> Reports -> Attendance Summary.
Filter parameters layout: select Job Sub Unit identifier tag value = "Sales", pick Date tracking range criteria. Click 'View'.
Expected Result: System generates summary charts matrix reflecting targeted tracking logs parameter dataset profiles cleanly.
6. Recruitment Module
TC-081: Verify creating a new Job Vacancy
Pre-conditions: Logged in as HR/Recruitment Manager. Path: Recruitment -> Vacancies.
Test Steps:
Click on the '+ Add' button layout element control link.
Select Job Title blueprint node string link, enter custom Title (e.g., "Senior DevOps Lead").
Assign Hiring Manager name user profile identity. Click 'Save'.
Expected Result: Vacancy establishes active data profile mappings, rendering status flag label indicator = "Active".
TC-082: Verify adding a new Candidate manually for a vacancy
Pre-conditions: Recruitment management panel dashboard workspace active. Path: Recruitment -> Candidates.
Test Steps:
Click '+ Add' button. Input candidate First Name, Last Name, active Contact Email string information.
Select specific target open vacancy position tracking item from dropdown list options. Click 'Save'.
Expected Result: Candidate identity tracks successfully inside repository, setting operational profile step identifier flag context status = "Application Initiated".
TC-083: Verify uploading candidate Resume
Pre-conditions: Adding/Editing candidate application record profile workspace window dashboard screen active.
Test Steps:
Drag or select a candidate file attachment document component block (e.g., resume.pdf).
Trigger file upload saving execution routines.
Expected Result: Archive saves alongside metadata profile container tracking layer cleanly without format structural breaking glitches.
TC-084: Verify changing Candidate Status to 'Shortlisted'
Pre-conditions: Candidate application profile profile workspace screen is active. Current stage status state structural flag = "Application Initiated".
Test Steps:
Click on action option tracking button layout component element labeled 'Shortlist'.
Enter tracking assessment note strings details background. Click 'Save'.
Expected Result: Profile state mapping transitions pipeline positions, updating stage dashboard indicators flags safely to 'Shortlisted'.
TC-085: Verify scheduling an Interview for a shortlisted candidate
Pre-conditions: Candidate pipeline state matches 'Shortlisted' criteria parameters step flags.
Test Steps:
Click on pipeline tracking tool action button item selector control labeled 'Schedule Interview'.
Provide custom Interview Name string label, assign specific Interviewer profile name tags, select Date & Time schedule calendar parameters. Click 'Save'.
Expected Result: System registers scheduling metadata details parameters, transitioning pipeline stage tracking indicator flag over to 'Interview Scheduled'.
TC-086: Verify marking Interview Status
Pre-conditions: Target candidate item currently flags status state metric identifier = "Interview Scheduled".
Test Steps:
Access candidate workflow view profile dashboard workspace screen pane.
Click on the 'Mark Interview Passed' action workflow control option element item link.
Input evaluation scores feedback data strings details. Click 'Save'.
Expected Result: System processes data modifications, moving lifecycle checkpoint markers tracking categories over to 'Interview Passed'.
TC-087: Verify changing Candidate Status to 'Offer Offered'
Pre-conditions: Candidate status path sequence milestone marks 'Interview Passed' track configuration step flags.
Test Steps:
Select action execution tool choice switch option component labeled 'Offer Job / Offer Salary'.
Fill custom text tracking notes description boxes parameters fields data. Save.
Expected Result: Stage tracking logs lifecycle position shifts indicators flags directly matching 'Offer Offered' phase mapping values.
TC-088: Verify changing Candidate Status to 'Hired' and linking to PIM
Pre-conditions: Candidate accepted current employment offer tracking parameters mappings configuration data.
Test Steps:
Click tracking action wizard tool control selection element step icon option labeled 'Hire Candidate'.
Complete onboarding profile structure details mapping layout interface options parameters. Click 'Save'.
Expected Result: Candidate record closes recruitment workflow phase tracking pipelines, generating matching fresh operational profile inside central PIM employee records table data repository.
TC-089: Verify Candidate Status 'Declined/Rejected'
Pre-conditions: Candidate profile actively evaluated anywhere inside processing stages tracking pipelines parameters layout workspace views.
Test Steps:
Click on action override choice management execution switch menu element button text labeled 'Reject Candidate'.
Pick reasons categorization configuration codes. Click 'Save'.
Expected Result: Application updates lifecycle track setting terminal flag parameters to 'Rejected', removing listing loops out active processing workspace queues dashboards.
TC-090: Verify searching vacancies by status
Pre-conditions: Recruitment module tracking panel dashboard grid overview page active.
Test Steps:
Locate search filter settings widget dropdown selection box component properties container labeled 'Status'.
Toggle value choice selection parameter item context index to 'Closed'. Click 'Search'.
Expected Result: Table records refresh, fetching exclusively old expired archival status job placement vacancy profiles list array rows data.
7. Performance & Dashboard Module
TC-091: Verify Key Performance Indicators (KPIs) creation for a specific job title
Pre-conditions: Admin/Performance Manager logged in. Path: Performance -> Configure -> KPIs.
Test Steps:
Click '+ Add'. Select specific target Job Title (e.g., "QA Engineer").
Input KPI parameter indicator identity string value text (e.g., "Code Coverage Ratio Execution").
Set Minimum metric value factor scaling indicator boundaries text scores (e.g., 0 to 100). Click 'Save'.
Expected Result: KPI mapping parameters lock down into corporate role evaluation frameworks metrics template systems array configuration logs safely.
TC-092: Verify creating a Performance Review tracker for an employee
Pre-conditions: Performance assessment criteria models configured across the organization framework. Path: Performance -> Manage Reviews -> Create Review.
Test Steps:
Provide specific Employee Name identity selection, fill timeline boundaries cycle date tracking tags.
Input Evaluators/Reviewers structural dependencies setup details metadata profiles parameters link names. Click 'Save' / 'Activate'.
Expected Result: Review workflow initiates, populating tracking status tables under 'In Progress' states.
TC-093: Verify Employee Self-Assessment rating submission
Pre-conditions: Performance Appraisal track record initiated. ESS employee role account dashboard session active.
Test Steps:
Path: Performance -> My Reviews. Open open active pending appraisal cycle form workspace.
Scroll down listing items parameters fields, modify scaling slider values numeric points selections or text assessment commentaries blocks.
Click 'Submit Evaluation'.
Expected Result: Form inputs capture securely, locking self-evaluation fields from future edits and passing task ownership over to reporting manager channels tracking.
TC-094: Verify Reviewer / Manager rating submission
Pre-conditions: Supervisor role logged in. Direct report worker self-assessment phase completed.
Test Steps:
Navigate configuration path layout menu tracking board: Performance -> Manage Reviews. Click on target employee appraisal form sheet view line item.
Fill separate distinct reviewer tracking evaluation calculation matrix rows text scoring areas. Click 'Complete Review'.
Expected Result: Appraisal cycle achieves total absolute milestone convergence, closing review workflows tracking loops transitioning state metrics indicators flags matching 'Finalized / Completed'.
TC-095: Verify Dashboard quick launch shortcuts functionality
Pre-conditions: User viewing main default system home workspace layout screen panel landing page view Dashboard.
Test Steps:
Locate graphic element panel container 'Quick Launch'. Click link navigation widget icon element tagged 'Assign Leave'.
Expected Result: Page redirects instantly loading corresponding tracking configuration forms module screens space without routing lag issues.
TC-096: Verify 'Employees on Leave Today' widget on dashboard
Pre-conditions: Active leave tracking entries matching system localization calendar current date exist in system database record lists rows.
Test Steps:
Access core landing default screen workspace Dashboard. Locate system tracking widget box panel titled 'Employees on Leave Today'.
Expected Result: Panel reflects accurate summarized visual profile cards list data tracking working names absent across enterprise sections layout grid view today.
TC-097: Verify 'Pending Leave Requests' notification widget for managers
Pre-conditions: Reporting supervisor role active dashboard view open. Direct reports have leaves awaiting manager review actions processing requests logs.
Test Steps:
Look at primary system dashboard summary workspace container dashboard views blocks.
Expected Result: System alert flags counter elements render numerical updates showing total actionable pending requests requiring structural approval oversight processing.
TC-098: Verify Buzz section social post creation
Pre-conditions: Social networking interaction functionality module 'Buzz' system option settings toggled active globally.
Test Steps:
Access application link workspace element menu choice item labeled 'Buzz'.
Type an announcement message string (e.g., "Celebrating successful project release cycle completion!") inside text post placeholder container text box. Click 'Post'.
Expected Result: Message text broadcasts instantly onto enterprise wide activity walls stream data grid dashboards feeds layouts.
TC-099: Verify liking/commenting on a Buzz post
Pre-conditions: Activity stream feeds display pre-existing text posts elements entries.
Test Steps:
Locate a team member's post. Click on the 'Like' icon element toggle component.
Move focus into text box row placeholder labeled 'Write a comment...', fill feedback message words, press Enter.
Expected Result: Interactive counters update calculations, displaying feedback comments structural layout beneath post logs array feed blocks safely.
TC-100: Verify deleting a self-created Buzz post
Pre-conditions: User has a previously created social update entry visible on their personal Buzz tracking workspace stream timeline.
Test Steps:
Locate personal message feed block inside stream timelines page panels. Click target contextual settings icon dropdown gear link element, choice select 'Delete Post'.
Authorize operation prompt choices confirmation dialog box popups text.
Expected Result: Target social feed elements tracking records map clears away completely, vanishing instantly out from central shared streaming timelines layers dashboard framework interfaces.