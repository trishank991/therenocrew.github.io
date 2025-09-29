# Google Forms Integration Setup Guide

## Step 1: Create Google Form

1. Go to [forms.google.com](https://forms.google.com)
2. Click "+ Blank" to create a new form
3. Title: "The Reno Crew - Free Quote Request"
4. Add these questions in this exact order:

### Question 1: First Name
- Type: Short answer
- Required: Yes

### Question 2: Last Name  
- Type: Short answer
- Required: Yes

### Question 3: Email
- Type: Short answer
- Required: Yes
- Validation: Email address

### Question 4: Phone
- Type: Short answer  
- Required: Yes

### Question 5: Service Required
- Type: Multiple choice
- Required: Yes
- Options:
  - Home Repairs
  - Deck Repair/Build
  - Renovations
  - Fencing
  - Lawn Care & Landscaping
  - Painting
  - GIB® & Plastering

### Question 6: Project Details
- Type: Paragraph
- Required: No
- Description: "Please describe your project requirements"

## Step 2: Get Form URLs and Entry IDs

1. **Get Form Action URL:**
   - In your Google Form, click "Send" button
   - Click the "<>" (link) icon
   - Copy the URL that appears
   - Change `/viewform` to `/formResponse` in the URL
   - This is your action URL

2. **Get Entry IDs:**
   - Right-click on your form page and select "View Page Source"
   - Search for "entry." in the page source
   - Find the entry IDs for each field (they look like entry.123456789)

## Step 3: Update Your Website

Replace these placeholders in your `index.html` file:

```
YOUR_GOOGLE_FORM_ACTION_URL → Your form action URL from step 2.1
entry.FIRST_NAME_ENTRY_ID → First name field entry ID
entry.LAST_NAME_ENTRY_ID → Last name field entry ID  
entry.EMAIL_ENTRY_ID → Email field entry ID
entry.PHONE_ENTRY_ID → Phone field entry ID
entry.SERVICE_ENTRY_ID → Service field entry ID
entry.PROJECT_DETAILS_ENTRY_ID → Project details field entry ID
```

## Step 4: Set Up Email Notifications

1. In your Google Form, click "Responses" tab
2. Click the three dots menu
3. Select "Get email notifications for new responses"
4. Check the box to receive notifications at `therenocrewltd@gmail.com`

## Step 5: View Responses

1. Responses will be collected in the "Responses" tab of your Google Form
2. You can also create a Google Sheet to collect responses:
   - In "Responses" tab, click the green sheet icon
   - Create a new spreadsheet to store all form submissions

## Example of what your final form action should look like:

```html
<form action="https://docs.google.com/forms/d/e/YOUR_FORM_ID/formResponse" method="POST" target="hidden_iframe">
```

## Testing

1. After updating the URLs and entry IDs, test your form
2. Submit a test quote request
3. Check your Google Form responses tab
4. Verify you receive an email notification

## Benefits

✅ Automatic data collection in Google Sheets  
✅ Email notifications for new submissions  
✅ Free to use  
✅ Secure and reliable  
✅ Easy to manage responses  
✅ Can set up automated responses to customers

## Need Help?

If you need assistance with finding the entry IDs or setting up the form, let me know and I can help you complete the integration.