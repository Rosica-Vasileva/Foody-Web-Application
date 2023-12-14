## Users should be able to access The Foody App from its designated URL via the internet, which should load the Home page, appropriate to the user's logged-in status (unregistered/non-logged or registered/logged).

### Use Case 1.1: Accessing Home Page as Unregistered/Non-Logged User

**Actors:**
- Guest (Unregistered/Non-Logged User)
- System

**Preconditions:**
- The Foody App is deployed and accessible via its designated URL on the internet.
- The user has an internet-connected device with a web browser.

**Main Flow:**

1. **Accessing the Home Page:**
   - The Guest opens a web browser.
   - Navigates to the designated URL of The Foody App.

2. **Detection of User Status:**
   - The Foody App recognizes the user as a Guest since they are not logged in.

3. **Loading Home Page for Unregistered/Non-Logged User:**
   - The system loads the Home Page appropriate for unregistered/non-logged users.
   - The Home Page may include features like exploring the app, viewing available restaurants, and signing up.

**Postconditions:**
- The Guest is presented with the Home Page tailored for unregistered/non-logged users.
- The user can navigate and interact with features available to non-logged users.

---

### Use Case 1.2: Accessing Home Page as Registered/Logged User

**Actors:**
- Registered User (Logged-In User)
- System

**Preconditions:**
- The Foody App is deployed and accessible via its designated URL on the internet.
- The user has an internet-connected device with a web browser.
- The user is registered and logged into The Foody App.

**Main Flow:**

1. **Accessing the Home Page:**
   - The Registered User opens a web browser.
   - Navigates to the designated URL of The Foody App.

2. **Recognition of Logged-In Status:**
   - The Foody App recognizes the user as registered/logged by checking their session status.

3. **User Authentication:**
   - The system authenticates the user's identity.

4. **Loading Home Page for Registered/Logged User:**
   - Upon successful authentication, the system loads the Home Page customized for registered/logged users.
   - The Home Page may include personalized features such as order history, favorites, and account settings.

**Postconditions:**
- The Registered User is presented with the Home Page customized for registered/logged users.
- The user can access personalized features and navigate the app as a logged-in user.



