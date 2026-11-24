## WebTracked Privacy Notice

WebTracked is a local analytics QA and journey-diagnostics browser extension. It is designed to record technical analytics evidence while a user deliberately runs a test journey through a website.

### Use test data only

WebTracked records captured analytics evidence unmasked. This can include data-layer values, analytics request query parameters and request bodies, and values that a website copies into its analytics implementation. If real customer or personal information is entered during a recorded journey and the website places that information into a data layer or analytics request, it may appear in WebTracked's locally stored journey and JSON export.

Use test data and test accounts only. Review an exported file before sharing it or uploading it to another service.

### What WebTracked records

While a journey is recording, WebTracked may record:

- page loads and route changes, including URL, page title, navigation information and referring page;
- supported data-layer contents and changes;
- supported tag-manager and analytics activity, including Adobe, Google/GTM/GA4 and Tealium activity;
- analytics network request URLs, query parameters and request bodies;
- user interactions used for analytics QA, such as the clicked element, visible click text and link target;
- OneTrust consent state where available;
- relevant failed tracking requests, network errors, script errors and Content Security Policy violations; and
- cookie metadata associated with the recorded journey.

WebTracked does not record keystrokes, screenshots, or raw cookie values. Cookie capture stores metadata such as the cookie name, domain, path, security attributes, whether a value exists and the value length. The cookie value itself is not stored.

Each export also records technical information identifying the WebTracked installation and build that produced it, including the extension ID, version and build identifier. These technical identifiers are not intended to identify an individual user. The wider journey export may contain personal information if such information was present in the website's data layer or analytics requests when the journey was recorded.

When WebTracked is not recording, it does not store journey evidence. Its page scripts are designed to remove their active hooks, polling and listeners after the extension confirms that no journey is being recorded. Some passive wrappers that were installed during the initial page load may remain in place and pass through without recording.

### Where the data goes

Captured journey data is stored locally in Chrome extension storage on the user's device. WebTracked does not transmit captured journey data to a WebTracked server or other external server.

A structured JSON export is created locally and downloaded only when the user chooses **JSON Export (AI-Ready)**. WebTracked does not automatically send or upload an export to an AI service. If a user chooses to upload or share an exported file with an AI tool or another service, that is a separate action controlled by the user or their organisation and is subject to that service's privacy and data-handling terms.

### Retention and deletion

By default, locally stored journey data is automatically deleted 7 days (168 hours) after a journey stops. An organisation administrator can configure a different retention period or turn automatic deletion off through managed browser policy.

Captured journey evidence is also removed when the user presses **Clear** or starts a new journey. Removing the extension or its stored browser data also removes locally stored WebTracked journey data.

Automatic deletion applies only to data stored by the extension. JSON files that have already been exported are separate files and must be deleted by the user or organisation that controls them.

### Organisation controls

An organisation administrator can restrict the websites on which WebTracked is allowed to record by using WebTracked's managed host policy. When such a restriction is configured, WebTracked refuses to start a journey on a website outside the approved list and discards captured evidence from non-approved sites. The JSON export indicates when an organisation host restriction applied.

### Permissions

WebTracked uses browser permissions only for its analytics QA and journey-testing purpose:

- **alarms**: runs scheduled checks for automatic deletion of locally stored journey data;
- **cookies**: reads cookie metadata for the website being tested. Raw cookie values are not stored;
- **storage**: stores journey evidence, settings and managed organisation policy locally in the browser;
- **tabs**: associates captured analytics evidence with the relevant browser tab, page and journey step;
- **webRequest**: observes supported analytics and tag-management network requests and related failures for QA evidence; and
- **host access to HTTPS websites**: allows WebTracked to carry out analytics QA on the user-selected websites and environments being tested, including journeys that cross domains.

### Selling, advertising and unrelated use

WebTracked does not sell captured journey data. WebTracked does not use captured journey data for advertising, profiling, determining creditworthiness or lending decisions, or for purposes unrelated to analytics QA and journey diagnostics.

### Important limitation

WebTracked is a technical QA tool and cannot determine whether information placed into a website's data layer or analytics requests is test data or real personal information. Users are responsible for using appropriate test data and for checking exported files before sharing them outside the browser.
