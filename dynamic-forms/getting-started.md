# Dynamic Forms: Getting Started

## How Does it All Work?

In short, you define one or more forms. Each form has a collection of controls (inputs) used to collect data from a user. Each form also contains a "routing script", which is used to make decisions like which form gets displayed next or to call external APIs to pass the user's data on to external systems.

## Creating a New Form

1. Log in to Dynamic Forms and click **NEW FORM DEFINITION** in the lower-right corner of the screen.

2. Provide a form name (we recommend a hierarchical naming format using colons as delimiters - example: `Support: Nexternal: Item Help`).

3. Provide a form ID (we recommend an all-lowercase version of your form name with spaces removed and underscores in place of colons - example: `support_nexternal_itemhelp`).

4. Click **CREATE**.

## Adding Controls to a Form

A dynamic form is simply a collection of controls used to gather data from the user. Each form MUST contain at lest one button unless it is intended to be the last form in a series. Without a button, users cannot move on to another form.

1. Click **ADD** under the **CONTROLS** tab and select the desired control type. See the [control types](/Home/Projects/Dynamic-Forms/Documentation/Control-Types) documentation for information on each available control type.

2. Change the control ID if desired. The ID is used as the key to access the control's data later on. ***If two controls in different forms share the same ID, the most recent control will overwrite the value from the previous one.***

3. Click **SAVE CHANGES** to ensure your new control(s) are saved to the form.

## How Routing Works

When a user clicks a button on a form, the form is "submitted" to the server. The platform will first save all of the data from the form's inputs using each control ID as the "key" for each value. After the data is saved, the form's routing script is evaluated. If an **onSubmit** function is defined in the script, the platform calls that function. The function must take care of either ending the session, displaying an error message to the user, or routing the user to the next form to be displayed. Please see the [routing script](/Home/Projects/Dynamic-Forms/Documentation/Routing-Scripts) documentation for more information.

## How Data is Stored for Later Use

While a session is active, the data provided by the user is stored in the platform database. This ensures sessions survive page refreshes and means sessions can be saved and continued later as well. Once a session is marked completed, the data is marked for deletion from the platform database. This means one of your routing scripts must pass the data you need on to an external service using a plugin. For more information on what plugins are available to use, please see the [plugin documentation](/Home/Projects/Dynamic-Forms/Documentation/Routing-Scripts/Plugins).
