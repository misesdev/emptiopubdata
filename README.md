## Here is where important information to be loaded into the emptio p2p app will be included.

* developers:
Developers, maintainers, or contributors who make contributions to the app's development can have personalized profiles within the app. 
This allows them to be available for anyone wishing to suggest changes, report issues, donate BTC, or have direct contact for questions 
and other information, thereby facilitating user access to developers and maintainers.

* securesellers:
Bitcoin sellers considered safe, so that users have direct access to purchasing bitcoin even without following sellers and buyers initially 
after creating an account or starting to use the emptio p2p app. These sellers will also be visible to all profiles and therefore must be 
considered safe, ensuring a guaranteed purchase for novice users with few contacts. Therefore, they must be validated before being added to this list. 
If you want to participate in this list, simply open an issue providing your nostr public key. After some validation processes, 
if you are deemed a safe seller, you will be added in the next commits.

* messages:
Alerts and messages to be displayed to users about the app and any announcements, enabling direct contact with all users in case of security issues or any other app-related problems.

### Returned JSON Format
`  { developers: [developerObjects..], securesellers: [sellerObjects..], messages: [messageObjects..], ... } `

### Developer Object Format
` { pubkey: "nostr public key - nip19", hierarchy: 1 } `

### Sellers Object Format
` { pubkey: "nostr public key - nip19", hierarchy: 1 } ` 

### Message Object Format
` { type: "alert", message: "hello" } `

### Types of Message

` "alert", "instruction" and "regular" `

#### To retrieve the information, simply execute a GET request as shown in the example with curl below

` curl https://emptioapp.github.io/emptiopubdata/index.json ` 
