# Intent Filters
### Criteria for an Activity's Intent Filter:
In order for a system to send an intent to an activity, the activity's intent filter must fulfill these three criteria:

1. **Action:** Defines the general action to be performed (e.g., view, edit, send).
2. **Data:** Specifies the type of data the activity can work with (e.g., specific MIME types or URIs).
3. **Category:** Describes additional information about the component handling the intent (e.g., default, browseable).

### Retrieving the Intent:
An activity retrieves the Intent that started it by calling `getIntent()` method within its code. This method returns the Intent object that was used to launch the activity.

### Intents Explained for a Non-technical Friend:

Imagine intents as messengers carrying requests or messages between different parts of an app or even between different apps on your phone. Each message (intent) has a purpose or action it wants something to do, like "open this picture" or "send this message."

These messages also come with some descriptions, like what kind of message it is and what it wants to work with (like a photo or a website link). Just like when you ask someone for help, you tell them what you need and maybe what you're giving them.

So, intents are like messengers that help different parts of your phone or different apps talk to each other by carrying specific requests or information.


# Implicit vs. Explicit Intents

**Implicit Intents:**
- **Purpose:** Used to request an action to be performed by any suitable component within the system.
- **Target:** Do not specify a particular component but instead declare a general action to be performed.
- **Example:** Asking the system to open a web page without specifying which browser to use.

**Explicit Intents:**
- **Purpose:** Used to specifically communicate with a particular component (activity, service, etc.) by its name.
- **Target:** Identifies the exact component that should handle the intent.
- **Example:** Launching a specific activity within an app to show user details.

### Primary Information in an Intent:

An Intent primarily contains:

1. **Action:** Describes the general action to be performed (e.g., view, edit, send).
2. **Data:** Specifies the data the action should operate on (e.g., a URI or MIME type).
3. **Component Information (for explicit intents):** Specifies the target component (e.g., the name of the activity or service).
4. **Extras:** Additional information bundled with the intent as key-value pairs.

This information helps the system understand what needs to be done and where it should be directed. For instance, an intent might convey a request to view a specific image (data) by opening a gallery app (action) and passing along the image's location (extra information).
