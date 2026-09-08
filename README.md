Solar Site Inspection App - README
Overview
A mobile-first web application for solar PV site inspections, designed for field engineers and solar installers to capture site data, photos, and sketches directly on-site. The app works offline, saves progress automatically, and exports professional inspection reports.

Key Features
📋 Smart Form
Section-based inspection form covering all aspects of a solar site assessment:

Project & customer information

Electrical supply & connection

Roof profile & mounting structure

Panel layout & shading analysis

Inverter & DC-side equipment

AC-side equipment & metering

Cabling (DC, AC & earthing)

Site access & logistics

Site photos checklist

Inspector remarks & sign-off

Conditional fields - additional questions appear when you answer "Yes" to having a second roof structure

Progress tracking - visual progress bar shows completion status

Auto-save - everything is saved locally as you type

📸 Photo & Sketch Capture
Photo checklist - mandatory photos for each inspection category (roof, DB, meter, inverter location, etc.)

Built-in sketch tool - draw site layouts directly on the canvas

Additional photos - capture any extra images not covered by the checklist

Photo storage - images are saved locally and included in exports

🏷️ BOQ Priority System
Priority levels - Normal, Priority, Urgent

Expected BOQ date - set a target completion date

Visual indicators - urgent items are highlighted in the header

📤 Export Options
Excel report - professionally formatted inspection report with all answers

Photo ZIP - download all captured photos in a single ZIP file

Combined bundle - Excel + photos in one shareable ZIP

Email composition - auto-generate an email with inspection summary

Data package - share complete inspection data (photos included) for import by colleagues

📁 History
Save inspections - store completed inspections locally

Group by inspector - entries are organized by who submitted them

Load previous - restore any past inspection into the form

Export from history - download Excel/photos from saved entries

Import data packages - receive inspection data from team members

Technical Requirements
Browser Support
Modern browsers with WebKit support (Chrome, Safari, Edge)

Mobile-first - optimized for phone use

iOS 14+ and Android 8+

Required Permissions
Camera/Photos - for capturing site photos

Location (GPS) - for capturing site coordinates

Local Storage - for saving drafts and history

Installation
Method 1: Web Launch (Quick Start)
Open the Solar_Site_Inspection_App.html file in any modern browser

For mobile: click "Add to Home Screen" in your browser menu

Method 2: Offline Use
This is a single HTML file with all resources embedded. No server is required. Simply open the HTML file in your browser.

How to Use
First Time Setup
Open the app

Enter your name when prompted (this labels your submissions)

You're ready to start inspecting!

Performing an Inspection
Fill in the form - work through each section

Tap the section header to expand/collapse

Required fields are indicated by the progress bar

Conditional fields appear automatically

Capture Photos

Tap the "Capture" or "Photo" button for each checklist item

Your camera will open

Photos are saved locally and associated with the inspection

For sketches: tap "Draw" to open the sketch tool

Set BOQ Priority

Choose Normal, Priority, or Urgent in the header

Set an expected BOQ date

Save Progress

Everything auto-saves as you type

The app is safe to close at any time

Complete the Form

All sections show a completion checkmark when done

The progress bar reaches 100%

Exporting
Basic Export
Tap "Download completed Excel" - saves a formatted Excel file

Tap "Download site photos (.zip)" - saves all photos in a ZIP

Combined Export
Tap "Share Excel + photos to WhatsApp / Email / etc."

The app creates a ZIP with both files

Your phone's share sheet opens - choose your app

Data Package (Import/Export)
Tap "Share data package" - creates a JSON file with all answers AND compressed photos

Share this with colleagues

They tap "Import a data package" to load it into their history

History Management
Tap "History" (top-right) or "View past inspections" (bottom)

Each saved inspection is shown in a card

From each card you can:

Share - export the inspection data

Download Excel - generate a report

Download photos - get all photos

Load into form - restore this inspection

Delete - remove from history

Email Reports
Tap "Compose email"

Auto-generated email with inspection summary opens in your email app

Manually attach the Excel and photos from your Downloads folder

Data Storage
Local Storage (IndexedDB)
Drafts - current inspection data saves automatically

History - completed inspections are stored

Photos - captured images are stored as blobs

Profile - your name is remembered

Data Persistence
Data survives closing the tab or switching apps

Works offline

No data is automatically uploaded anywhere

Photos are stored only on your device

Clearing Data
"Clear form" - removes current draft, keeps history

Delete from History - removes individual saved entries

File Formats
Format	Use	Compatibility
.xlsx	Excel inspection report	Excel, LibreOffice, Google Sheets
.zip	Photo bundle / Combined bundle	Any ZIP extractor
.sitepkg.json	Data package for import	App-only JSON format
Troubleshooting
Photos Not Saving
Check browser permissions (Settings > Camera)

Ensure you have sufficient device storage

Try a different browser (Chrome is recommended)

Location Not Working
Check GPS/Location is enabled on your device

Grant location permission to the browser

Mobile data or WiFi must be on (for GPS assistance)

Can't Find Exported Files
Check your Downloads folder

For mobile: check Files app > Downloads

The app saves files directly, not to cloud storage

File Opens as .bin Instead of .xlsx
This can happen in WebView wrappers - use a full browser

The app still saves the file to Downloads correctly

Rename the file from .bin to .xlsx if needed

App Not Saving Between Sessions
This requires a real browser (not an in-app preview)

Add the app to your home screen for best results

Check that IndexedDB is available in your browser

Development Notes
Architecture
Single HTML file - all CSS and JavaScript embedded

IndexedDB - for local storage

ExcelJS - for styled Excel export

SheetJS (XLSX) - fallback export

JSZip - for creating ZIP files

Canvas API - for sketch tool

Conditional Logic
conditional field attribute controls visibility

Field appears when parent field = "Yes"

The isConditionallyVisible() function handles this

Photo Management
Photos stored as photo:{id} in IndexedDB

Each photo has blob data and filename

Sketch images are handled as PNG blobs

Extra photos use generated IDs

Credits
This app is designed for solar installers and site inspectors who need a reliable, offline-first tool for collecting site data.

Quick Reference: Export Methods
Button	Output	Use Case
Share Excel + photos	ZIP (Excel + all photos)	Send complete package to BOQ team
Download completed Excel	.xlsx file	Office/Excel report
Download site photos	.zip file	Share images separately
Compose email	Email draft	Send summary with attachments
Share data package	.sitepkg.json	Import by colleagues
Save to history	Local stored	Keep record for later
Last Updated: November 2024
Version: 2.0
For support: Refer to the app's built-in help or contact your system administrator.
