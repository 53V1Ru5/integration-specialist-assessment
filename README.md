***Application Instructions:***

Please review all 4 tasks outlined below and submit 4 completed tasks

[**Task One:**](#task-one)

Create a button on an HTML page. When you click that button, an event should be sent into Google Tag Manager. Configure Google Tag Manager to send the trigger into Google Analytics. Create and configure a goal in Google Analytics so you can display said event as a conversion. Use [loom.com](https://www.loom.com) to take a video of the process from end to end with the conversion showing up in Google Analytics.

**Task Two:**

Create an HTML form that pushes lead information (name, email, and phone) into Zapier. Check if the email and phone are valid using a regular expression in Zapier, and then create a record in Google Sheets if they are. Use [loom.com](https://www.loom.com) to take a video of the process from end to end.

**Task Three:**

Use Postman and our API to submit a lead into our backend and record it via Loom. If you run into an error, please use your knowledge of APIs and our documentation to work around any errors.

API Key: `OrmWlwX1.7ER0jXF6rUcHKwfH2rfYdLgDN6aQefal`

Community ID: `12636`

Success looks like:
```json
{
   "success": "Created new Lead"
}
```

**Task Four:**

Please use CSS to style your project in a way that is aesthetically pleasing, simple, and creates a great user experience.


## Task One
### Instructions to Create a Button and Track Event in Google Tag Manager

1. **Set up Google Tag Manager:**
   - Create a Google Tag Manager account and container.
   - Retrieve the container code snippet provided by Google Tag Manager and add it to the `<head>` section of your HTML page.

2. **Create the button:**
   - In your HTML file, add a button element using the `<button>` tag.
   - Give the button an ID to make it easy to identify in JavaScript.
   ```html
   <button id="myButton">Click Me!</button>
   ```

3. **Add JavaScript code:**
   - Place the following JavaScript code just before the closing `</body>` tag or in an external JavaScript file.
   - Replace `'YOUR_TRIGGER_NAME'` with the name of the trigger you want to send to Google Analytics.
   ```html
   <script>
     document.getElementById('myButton').addEventListener('click', function() {
       // Push the event data to Google Tag Manager data layer
       window.dataLayer = window.dataLayer || [];
       window.dataLayer.push({
         'event': 'YOUR_TRIGGER_NAME'
       });
     });
   </script>
   ```

4. **Configure Google Tag Manager:**
   - Log in to your Google Tag Manager account and navigate to your container.
   - Create a new trigger:
     - Click on "Triggers" in the left sidebar.
     - Click on "New" to create a new trigger.
     - Choose a trigger type based on your requirements, such as a "Click" trigger or a custom trigger.
     - Configure the trigger settings according to your button's ID or other criteria.
     - Save the trigger.

5. **Connect Google Tag Manager to Google Analytics:**
   - Navigate to "Tags" in the left sidebar.
   - Click on "New" to create a new tag.
   - Give your tag a descriptive name.
   - Choose the tag type as "Google Analytics: Universal Analytics" or "Google Analytics: GA4 Configuration" based on your setup.
   - Configure the tag with your Google Analytics tracking ID or other settings as needed.
   - Under "Triggering", select the trigger you created earlier.
   - Save the tag.

6. **Publish and test:**
   - Click on "Submit" in the top-right corner of Google Tag Manager to publish your changes.
   - Test the button by clicking it on your HTML page.
   - Verify if the event is being captured in Google Analytics by checking the Real-Time reports or the Events reports.

### Instructions to Create a Goal in Google Analytics

1. **Log in to your Google Analytics account.**
2. **Go to the "Admin" section.**
3. **In the "View" column, click on "Goals".**
4. **Click on "+ New Goal" to create a new goal.**
5. **Choose a goal template or create a custom goal.**
6. **Provide a name and select the appropriate goal details.**
7. **In the "Goal Details" section, set the event conditions that match the event triggered by the button.**
8. **Save the goal.**

Now, when users click the button, the event will be sent to Google Tag Manager, which will trigger the tag associated with Google Analytics. The event will then be tracked as a conversion based on the configured goal in Google Analytics.


## Google Analytics