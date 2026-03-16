# Setup Guide - LinkedIn Content Scheduler

## Step 1: Copy Google Sheet Template (5 min)

1. Open template: [LinkedIn Content Calendar](YOUR-SHEET-LINK)
2. File → Make a copy
3. Name it: "My LinkedIn Calendar"

## Step 2: Add Your Content (10 min)

Sample week of posts:

**Monday:**
```
Date: [Next Monday]
Post Text: 🚀 Kicking off the week with a new automation project...
Status: Ready
```

**Wednesday:**
```
Date: [Next Wednesday]
Post Text: 3 lessons learned from building n8n workflows...
Status: Ready
```

**Friday:**
```
Date: [Next Friday]
Post Text: Week in review: Shipped X projects, learned Y lessons...
Status: Ready
```

## Step 3: Import Workflow to n8n (5 min)

1. Download: `workflows/linkedin-scheduler-workflow.json`
2. n8n → Import from File
3. Set Google Sheets credentials
4. Update Sheet ID in "Fetch Today's Posts" node

## Step 4: Test (5 min)

1. Set one post's date to TODAY
2. Set status to "Ready"
3. Execute workflow manually
4. Check Sheet - should update Post URL, Published At, Status

## Step 5: Activate (1 min)

1. Toggle workflow ON
2. Posts will auto-process daily at 9am Lagos time

## Step 6: Daily Routine (Manual LinkedIn Posting)

Since we're using simulated publishing:

1. Check Google Sheet at 9:05am
2. Find rows with Status = "Published"
3. Copy "Post Text"
4. Manually paste to LinkedIn
5. After publishing, copy real LinkedIn post URL
6. Paste into "Post URL" column

**Future improvement:** Integrate Zapier/Make webhook for true auto-publishing.
