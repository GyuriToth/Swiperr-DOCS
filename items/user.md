# **User Specification**

## Description

The user can be anyone show accesses the swipper system at any given point.
Access rights and properties are derived from the role of the user.

## Roles and Rights

- Unregistrated user (Guest)
- Registrated user (Member)
- Support (Moderator)
- Administrator (Admin)


| **Feature / Action**           | **Guest (Unregistered)** | **Member (Registered)** | **Support (Moderator)** | **Admin (Administrator)** |
| ------------------------------ | ------------------------ | ----------------------- | ----------------------- | ------------------------- |
| **View public content**        | ✅ Yes                    | ✅ Yes                   | ✅ Yes                   | ✅ Yes                     |
| **Register / Login**           | ✅ Yes                    | ❌ No                    | ❌ No                    | ❌ No                      |
| **Edit own profile**           | ❌ No                     | ✅ Yes                   | ✅ Yes                   | ✅ Yes                     |
| **Post content / comments**    | ❌ No                     | ✅ Yes                   | ✅ Yes                   | ✅ Yes                     |
| **Edit own content**           | ❌ No                     | ✅ Yes                   | ✅ Yes                   | ✅ Yes                     |
| **Report content**             | ❌ No                     | ✅ Yes                   | ✅ Yes                   | ✅ Yes                     |
| **Moderate user content**      | ❌ No                     | ❌ No                    | ✅ Yes                   | ✅ Yes                     |
| **Suspend users**              | ❌ No                     | ❌ No                    | ✅ Yes                   | ✅ Yes                     |
| **Manage roles & permissions** | ❌ No                     | ❌ No                    | ❌ No                    | ✅ Yes                     |
| **Access admin dashboard**     | ❌ No                     | ❌ No                    | ✅ Limited               | ✅ Full                    |
| **Site settings**              | ❌ No                     | ❌ No                    | ❌ No                    | ✅ Yes                     |
| **Manage users**               | ❌ No                     | ❌ No                    | ✅ Limited               | ✅ Full                    |





**Guest**

A visitor viewing the webpage or the application without an account.
Guest must have the most restricted access to the system.

TODO: fill this

**Member**

A registrated user, it can authenticate with the credentials stored in the internal database.

TODO: fill this

**Support (Moderator)**

Support user, managing users and content.

Responsibilities:
- Edit or delete inappropriate posts/comments.
- Suspend or warn users.
- No access to core application settings.

TODO: fill this

**Administrator**

Responsibilities:
- Add/remove users.
- Configure settings.
- Manage roles and permissions.
- Access analytics and reports.

TODO: fill this

---

### Properties

#TODO: refine this
All information corresponding with all features of the users.

* **UID**

  * *Type:* `string` (UUID or numeric ID)
  * *Description:* Unique identifier for each user.
  * *Required:* Yes

* **Username**

  * *Type:* `string`
  * *Description:* Unique display name for login and identification.
  * *Required:* Yes

* **Password**

  * *Type:* `string` (hashed & salted)
  * *Description:* Authentication credential.
  * *Required:* Yes
  * *Security:* Must be encrypted before storage.

* **E-mail**

  * *Type:* `string` (valid email format)
  * *Description:* Primary contact email.
  * *Required:* Yes
  * *Constraints:* Must be unique.

---

### **Personal Details**

* **Surname**

  * *Type:* `string`
  * *Description:* First name of the user.
  * *Required:* Yes

* **Last name**

  * *Type:* `string`
  * *Description:* Family name of the user.
  * *Required:* Yes

* **Birthdate**

  * *Type:* `date`
  * *Description:* Date of birth (YYYY-MM-DD).
  * *Required:* Optional
  * *Use case:* Age verification, personalization.

* **Gender**

  * *Type:* `enum` (`Male`, `Female`, `Other`, `Prefer not to say`)
  * *Description:* Gender identification.
  * *Required:* Optional

---

### **Contact Information**

* **Address**

  * *Type:* `string`
  * *Description:* Residential address.
  * *Required:* Optional

* **Phone number**

  * *Type:* `string` (E.164 format recommended, e.g., +123456789)
  * *Description:* Contact phone number.
  * *Required:* Optional

---

### **Profile Information**

* **Profile Picture**

  * *Type:* `string` (URL or file path)
  * *Description:* Link to the user’s avatar.
  * *Required:* Optional

* **Works/Studies**

  * *Type:* `string`
  * *Description:* Current workplace or educational institution.
  * *Required:* Optional

* **BIO**

  * *Type:* `string` (max length e.g., 250 chars)
  * *Description:* Short personal description.
  * *Required:* Optional

---

### **Roles & Permissions**

* **Role**

  * *Type:* `enum`
  * *Allowed Values:*

    * `guest` – Unregistered user with basic viewing permissions.
    * `member` – Registered user with standard interaction capabilities.
    * `support` – Moderator role with content moderation rights.
    * `admin` – Full administrator with complete system control.
  * *Default:* `guest`
  * *Required:* Yes

---

#### **Additional Notes**

* Passwords **must be hashed** using a strong algorithm (e.g., `bcrypt`, `argon2`).
* Use **email verification** for account activation.
* Consider **GDPR compliance** for personal data handling.
* Ensure **phone number validation** for formats and optional SMS verification.

---

### **Features**

TODO: write or link here all features of each user role

---



