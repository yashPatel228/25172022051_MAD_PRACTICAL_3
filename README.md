# Android Implicit and Explicit Intent Application

![Android](https://img.shields.io/badge/Platform-Android-green)
![Language](https://img.shields.io/badge/Language-Kotlin-blue)
![UI](https://img.shields.io/badge/UI-XML-orange)
![IDE](https://img.shields.io/badge/IDE-Android%20Studio-lightgrey)
![License](https://img.shields.io/badge/License-Educational-lightgrey)

An Android application developed using **Kotlin and XML** to demonstrate **Implicit Intent and Explicit Intent**.

The application allows the user to perform different Android operations such as making a call, opening a URL, viewing the Call Log, opening the Gallery, setting an alarm, opening the Camera, and navigating to a Login Activity.

This practical also demonstrates **Intent Actions, Intent.setData(), Intent.setType(), Uri.parse(), Permissions, ActivityResultContracts, ConstraintLayout, CoordinatorLayout, and startActivity()**.

---

## 📌 Practical Information

| Field                      | Details                        |
| -------------------------- | ------------------------------ |
| **Subject**                | Mobile Application Development |
| **Practical No.**          | 3                              |
| **Practical Title**        | Implicit & Explicit Intent     |
| **Student Enrollment No.** | 25172022051                    |
| **Programming Language**   | Kotlin                         |
| **UI Technology**          | XML                            |
| **Development Tool**       | Android Studio                 |
| **Repository**             | `25172022051_MAD_PRACTICAL_3`  |

---

## 🎯 Aim

To create an Android application which demonstrates **Implicit & Explicit Intent**.

---

## 📖 Introduction

An **Intent** is a messaging object used in Android to request an action from another application component.

Intents are commonly used to:

* Start an Activity.
* Open another application.
* Send data between Activities.
* Perform actions such as making a call or opening a URL.

This practical demonstrates both **Implicit Intent** and **Explicit Intent**.

---

## ✨ Features

The application provides the following operations:

1. Make a call to a specific number.
2. Open a specific URL.
3. Open the Call Log.
4. Open the Gallery.
5. Set an Alarm.
6. Open the Camera.
7. Open the Login Activity.

Additional features:

* Uses **Implicit Intent** for external Android operations.
* Uses **Explicit Intent** for opening Login Activity.
* Uses **Intent.setData()**.
* Uses **Intent.setType()**.
* Uses **Uri.parse()**.
* Uses **Button**.
* Uses **ConstraintLayout**.
* Uses **CoordinatorLayout**.
* Uses **startActivity()**.
* Uses **ActivityResultContracts**.
* Uses **ContextCompat.checkSelfPermission()**.
* Uses **ActivityCompat.requestPermissions()**.
* Uses required permissions in `AndroidManifest.xml`.

---

## 🛠️ Technologies Used

* **Android Studio**
* **Kotlin**
* **XML**
* **Android SDK**
* **Intent**
* **Implicit Intent**
* **Explicit Intent**
* **Button**
* **ConstraintLayout**
* **CoordinatorLayout**
* **ActivityResultContracts**
* **Uri.parse()**
* **Intent.setData()**
* **Intent.setType()**
* **startActivity()**
* **Android Permissions**
* **Camera**
* **Gallery**
* **Call Log**
* **AlarmManager**

---

## 🎨 User Interface

The application contains buttons for performing different Intent operations.

### Main UI Components

| Component             | Purpose                              |
| --------------------- | ------------------------------------ |
| **Button**            | Performs an Intent operation         |
| **ConstraintLayout**  | Arranges UI components               |
| **CoordinatorLayout** | Provides a flexible layout structure |
| **TextView**          | Displays labels or instructions      |
| **Login Activity**    | Demonstrates Explicit Intent         |

### Example UI

```text
┌──────────────────────────────┐
│                              │
│       INTENT APPLICATION      │
│                              │
│  ┌────────────────────────┐  │
│  │   Make Call            │  │
│  └────────────────────────┘  │
│                              │
│  ┌────────────────────────┐  │
│  │   Open URL             │  │
│  └────────────────────────┘  │
│                              │
│  ┌────────────────────────┐  │
│  │   Open Call Log        │  │
│  └────────────────────────┘  │
│                              │
│  ┌────────────────────────┐  │
│  │   Open Gallery         │  │
│  └────────────────────────┘  │
│                              │
│  ┌────────────────────────┐  │
│  │   Set Alarm            │  │
│  └────────────────────────┘  │
│                              │
│  ┌────────────────────────┐  │
│  │   Open Camera          │  │
│  └────────────────────────┘  │
│                              │
│  ┌────────────────────────┐  │
│  │   Open Login Activity  │  │
│  └────────────────────────┘  │
│                              │
└──────────────────────────────┘
```

> **Note:** The exact UI depends on the XML layout implemented in the project.

---

## 📚 What is Intent?

An **Intent** is used to communicate between Android components.

It can be used to:

* Start an Activity.
* Open another application.
* Send data.
* Request an action from the Android system.

### Example

```kotlin
val intent = Intent(this, LoginActivity::class.java)
startActivity(intent)
```

---

## 🔀 Types of Intent

Android Intents are mainly divided into two types:

### 1. Implicit Intent

An **Implicit Intent** does not specify the exact component to be started.

Instead, it specifies an action that another application or Android system can perform.

### Example

```kotlin
val intent = Intent(Intent.ACTION_VIEW)
intent.data = Uri.parse("https://www.google.com")
startActivity(intent)
```

This opens a suitable application for the URL.

### Uses

* Open URL.
* Open Gallery.
* Open Camera.
* Set Alarm.
* Open Call Log.
* Make a Call.

---

### 2. Explicit Intent

An **Explicit Intent** specifies the exact Activity or component to be started.

### Example

```kotlin
val intent = Intent(this, LoginActivity::class.java)
startActivity(intent)
```

### Uses

* Open Login Activity.
* Navigate between Activities.
* Pass data between Activities.

---

## 🔄 Implicit vs Explicit Intent

| Feature         | Implicit Intent              | Explicit Intent                           |
| --------------- | ---------------------------- | ----------------------------------------- |
| **Component**   | Not specified directly       | Specified directly                        |
| **Purpose**     | Requests an action           | Starts a specific component               |
| **Example**     | Open URL                     | Open Login Activity                       |
| **Application** | May open another app         | Usually opens own app component           |
| **Action**      | `ACTION_VIEW`, `ACTION_CALL` | `Intent(this, LoginActivity::class.java)` |

---

## 🧩 Intent Actions

Intent Actions specify the operation to be performed.

### Common Intent Actions

| Intent Action             | Purpose                                        |
| ------------------------- | ---------------------------------------------- |
| `Intent.ACTION_CALL`      | Makes a phone call                             |
| `Intent.ACTION_VIEW`      | Opens a URL or other content                   |
| `Intent.ACTION_PICK`      | Selects an item from another application       |
| `Intent.ACTION_SET_ALARM` | Opens the alarm application                    |
| `Intent.ACTION_MAIN`      | Defines the main entry point of an application |

---

## 📱 Practical Operations

## 1. Make Call to Specific Number

This operation uses an **Implicit Intent** to make a call.

### Intent Action

```kotlin
Intent.ACTION_CALL
```

### URI Scheme

```text
tel:
```

### Example

```kotlin
val intent = Intent(Intent.ACTION_CALL)
intent.data = Uri.parse("tel:9876543210")
startActivity(intent)
```

### Explanation

* `ACTION_CALL` requests a phone call.
* `tel:` specifies the telephone number.
* `Uri.parse()` converts the String into a URI.
* `startActivity()` starts the action.

### Permission

```xml
<uses-permission android:name="android.permission.CALL_PHONE" />
```

> **Note:** `ACTION_CALL` requires the `CALL_PHONE` permission. On Android, the user must grant the permission before the call can be made.

---

## 2. Open Specific URL

This operation uses an **Implicit Intent** to open a URL.

### Intent Action

```kotlin
Intent.ACTION_VIEW
```

### Example

```kotlin
val intent = Intent(Intent.ACTION_VIEW)
intent.data = Uri.parse("https://www.google.com")
startActivity(intent)
```

### Explanation

* `ACTION_VIEW` requests to view content.
* `Uri.parse()` converts the URL into a URI.
* Android opens a suitable browser.

### URI Example

```text
https://www.google.com
```

---

## 3. Open Call Log

This operation uses an **Implicit Intent** to open the Call Log.

### Intent Action

```kotlin
Intent.ACTION_VIEW
```

### Content Type

```kotlin
CallLog.Calls.CONTENT_TYPE
```

### Example

```kotlin
val intent = Intent(Intent.ACTION_VIEW)
intent.data = Uri.parse("content://call_log/calls")
startActivity(intent)
```

### Explanation

* `ACTION_VIEW` requests to view content.
* The Call Log URI identifies the call history.
* Android opens a suitable application.

### Study Constant

```kotlin
CallLog.Calls.CONTENT_TYPE
```

---

## 4. Open Gallery

This operation uses an **Implicit Intent** to open the Gallery or image picker.

### Intent Action

```kotlin
Intent.ACTION_PICK
```

### Content Type

```kotlin
"image/*"
```

### Example

```kotlin
val intent = Intent(Intent.ACTION_PICK)
intent.type = "image/*"
startActivity(intent)
```

### Explanation

* `ACTION_PICK` requests the user to select an item.
* `"image/*"` specifies that images are required.
* Android opens a suitable Gallery or image picker.

### Alternative

```kotlin
Intent.ACTION_GET_CONTENT
```

---

## 5. Set Alarm

This operation uses an **Implicit Intent** to open the Alarm application.

### Intent Action

```kotlin
Intent.ACTION_SET_ALARM
```

### Example

```kotlin
val intent = Intent(AlarmClock.ACTION_SET_ALARM)

intent.putExtra(
    AlarmClock.EXTRA_MESSAGE,
    "Wake Up"
)

intent.putExtra(
    AlarmClock.EXTRA_HOUR,
    7
)

intent.putExtra(
    AlarmClock.EXTRA_MINUTES,
    30
)

startActivity(intent)
```

### Explanation

* `ACTION_SET_ALARM` requests an alarm.
* `EXTRA_MESSAGE` specifies the alarm label.
* `EXTRA_HOUR` specifies the hour.
* `EXTRA_MINUTES` specifies the minutes.

### Required Import

```kotlin
import android.provider.AlarmClock
```

---

## 6. Open Camera

This operation uses an **Implicit Intent** to open the Camera application.

### Intent Action

```kotlin
MediaStore.ACTION_IMAGE_CAPTURE
```

### Example

```kotlin
val intent = Intent(MediaStore.ACTION_IMAGE_CAPTURE)
startActivity(intent)
```

### Explanation

* `ACTION_IMAGE_CAPTURE` requests image capture.
* Android opens a suitable Camera application.

### Permission

```xml
<uses-permission android:name="android.permission.CAMERA" />
```

> **Note:** If the application only launches an external camera application using an Intent, camera permission may not be required by the calling app. If the app directly accesses the camera, the `CAMERA` permission is required.

---

## 7. Open Login Activity

This operation uses an **Explicit Intent**.

### Example

```kotlin
val intent = Intent(this, LoginActivity::class.java)
startActivity(intent)
```

### Explanation

* `this` refers to the current Activity.
* `LoginActivity::class.java` specifies the exact Activity.
* `startActivity()` opens LoginActivity.

### Purpose

* Demonstrates Explicit Intent.
* Navigates from MainActivity to LoginActivity.

---

## 📤 Intent.setData()

`setData()` is used to set the data URI of an Intent.

### Example

```kotlin
val intent = Intent(Intent.ACTION_VIEW)
intent.setData(Uri.parse("https://www.google.com"))
startActivity(intent)
```

### Purpose

* Sets the data to be acted upon.
* Used for URLs, telephone numbers, and content URIs.

---

## 🗂️ Intent.setType()

`setType()` is used to specify the MIME type of the data.

### Example

```kotlin
val intent = Intent(Intent.ACTION_PICK)
intent.setType("image/*")
startActivity(intent)
```

### Purpose

* Specifies the type of content.
* Used when selecting images, videos, documents, etc.

---

## 🔗 Uri.parse()

`Uri.parse()` converts a String into a URI object.

### Example

```kotlin
val uri = Uri.parse("https://www.google.com")
```

### Purpose

* Converts a URL or URI String.
* Used with `Intent.setData()`.

---

## ▶️ startActivity()

`startActivity()` is used to start another Activity or perform an Intent action.

### Example

```kotlin
startActivity(intent)
```

### Purpose

* Opens another Activity.
* Opens external applications.
* Performs Intent actions.

---

## 🔐 Permissions in Android

Some Android operations require permissions.

Permissions are declared in the `AndroidManifest.xml` file.

### Example

```xml
<uses-permission android:name="android.permission.CALL_PHONE" />
```

### Common Permissions

| Permission      | Purpose                         |
| --------------- | ------------------------------- |
| `CALL_PHONE`    | Make phone calls                |
| `CAMERA`        | Access camera                   |
| `READ_CALL_LOG` | Read call history when required |

> **Note:** Permission requirements depend on the Android version and the exact API used. Some operations, such as opening a Gallery or external Camera app, may not require the calling app to request the corresponding permission.

---

## 🛡️ ContextCompat.checkSelfPermission()

`ContextCompat.checkSelfPermission()` checks whether a permission has been granted.

### Example

```kotlin
if (
    ContextCompat.checkSelfPermission(
        this,
        Manifest.permission.CALL_PHONE
    ) == PackageManager.PERMISSION_GRANTED
) {
    // Permission granted
}
```

### Purpose

* Checks permission status.
* Prevents unauthorized access.

---

## 📥 ActivityCompat.requestPermissions()

`ActivityCompat.requestPermissions()` requests permission from the user.

### Example

```kotlin
ActivityCompat.requestPermissions(
    this,
    arrayOf(Manifest.permission.CALL_PHONE),
    100
)
```

### Purpose

* Requests runtime permissions.
* Allows the user to grant or deny permission.

---

## 📦 ActivityResultContracts

`ActivityResultContracts` is used to handle results returned from Activities.

It provides a modern way to launch Activities and receive results.

### Example

```kotlin
private val pickImage =
    registerForActivityResult(
        ActivityResultContracts.GetContent()
    ) { uri ->
        // Selected image URI
    }
```

### Launch

```kotlin
pickImage.launch("image/*")
```

### Purpose

* Opens another Activity.
* Receives results.
* Handles Gallery and other Activity results.

---

## 🖼️ Gallery using ActivityResultContracts

### Example

```kotlin
private val pickImage =
    registerForActivityResult(
        ActivityResultContracts.GetContent()
    ) { uri ->
        if (uri != null) {
            // Display selected image
        }
    }
```

### Launch

```kotlin
pickImage.launch("image/*")
```

### Explanation

* `GetContent()` opens a content picker.
* `"image/*"` specifies image content.
* The selected URI is returned in the callback.

---

## 📷 Camera using ActivityResultContracts

### Example

```kotlin
private val takePicture =
    registerForActivityResult(
        ActivityResultContracts.TakePicturePreview()
    ) { bitmap ->
        if (bitmap != null) {
            // Display captured image
        }
    }
```

### Launch

```kotlin
takePicture.launch(null)
```

### Explanation

* `TakePicturePreview()` captures a preview image.
* The result is returned as a Bitmap.

---

## 🎨 ConstraintLayout

`ConstraintLayout` is used to arrange UI elements using constraints.

### Example

```xml
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

</androidx.constraintlayout.widget.ConstraintLayout>
```

### Purpose

* Arranges UI components.
* Supports responsive layouts.
* Positions views using constraints.

---

## 🧩 CoordinatorLayout

`CoordinatorLayout` is a layout used to coordinate interactions between child views.

### Example

```xml
<androidx.coordinatorlayout.widget.CoordinatorLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

</androidx.coordinatorlayout.widget.CoordinatorLayout>
```

### Purpose

* Coordinates child views.
* Supports Material Design components.
* Used for flexible UI layouts.

---

## 📂 Project Structure

```text
25172022051_MAD_PRACTICAL_3/
│
├── .idea/
│
├── app/
│   └── src/
│       └── main/
│           │
│           ├── java/
│           │   └── com/
│           │       └── example/
│           │           └── a25172022051_MAD_PRACTICAL_3/
│           │               │
│           │               ├── MainActivity.kt
│           │               └── LoginActivity.kt
│           │
│           ├── res/
│           │   ├── layout/
│           │   │   ├── activity_main.xml
│           │   │   └── activity_login.xml
│           │   │
│           │   ├── drawable/
│           │   │   └── application_drawables.xml
│           │   │
│           │   └── values/
│           │       ├── colors.xml
│           │       ├── strings.xml
│           │       └── themes.xml
│           │
│           └── AndroidManifest.xml
│
├── gradle/
│
├── build.gradle.kts
├── settings.gradle.kts
├── gradle.properties
├── gradlew
├── gradlew.bat
└── README.md
```

> **Note:** The actual package name and file names may differ depending on the project implementation.

---

## 📄 MainActivity.kt Responsibilities

`MainActivity.kt` is responsible for:

* Initializing the Activity.
* Connecting the XML layout with the Activity.
* Displaying the main UI.
* Handling button clicks.
* Creating Implicit Intents.
* Creating Explicit Intents.
* Opening URLs.
* Making phone calls.
* Opening Call Log.
* Opening Gallery.
* Setting Alarm.
* Opening Camera.
* Opening Login Activity.
* Checking permissions.
* Requesting permissions.
* Handling Activity results.

---

## 📄 LoginActivity.kt Responsibilities

`LoginActivity.kt` is responsible for:

* Displaying the Login Activity.
* Demonstrating Explicit Intent navigation.
* Providing the login interface.

---

## 📄 activity_main.xml Responsibilities

`activity_main.xml` is responsible for:

* Creating the main UI.
* Displaying buttons.
* Arranging UI components.
* Providing controls for Intent operations.

---

## 📄 activity_login.xml Responsibilities

`activity_login.xml` is responsible for:

* Creating the Login Activity UI.
* Displaying login-related components.

---

## 📄 AndroidManifest.xml Responsibilities

`AndroidManifest.xml` is responsible for:

* Registering Activities.
* Declaring permissions.
* Setting the launcher Activity.

### Example

```xml
<uses-permission android:name="android.permission.CALL_PHONE" />
<uses-permission android:name="android.permission.CAMERA" />

<application
    ...>

    <activity
        android:name=".LoginActivity"
        android:exported="false" />

    <activity
        android:name=".MainActivity"
        android:exported="true">

        <intent-filter>
            <action android:name="android.intent.action.MAIN" />
            <category android:name="android.intent.category.LAUNCHER" />
        </intent-filter>

    </activity>

</application>
```

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/yashPatel228/25172022051_MAD_PRACTICAL_3.git
```

### Step 2: Open the Project

Open the cloned project in **Android Studio**.

### Step 3: Wait for Gradle Sync

Allow Android Studio to complete the Gradle synchronization.

### Step 4: Connect a Device

Connect an Android device using USB debugging or start an Android Emulator.

> **Note:** For testing phone calls, Camera, and other device-dependent operations, a physical Android device may provide a better experience.

### Step 5: Run the Application

Click the **Run ▶️** button in Android Studio.

### Step 6: Test Intent Operations

Click each button and observe the corresponding operation.

---

## 📊 Expected Output

### Main Activity

```text
Intent Application

[ Make Call ]
[ Open URL ]
[ Open Call Log ]
[ Open Gallery ]
[ Set Alarm ]
[ Open Camera ]
[ Open Login Activity ]
```

### Make Call

The phone application opens with the specified number.

### Open URL

The browser opens the specified URL.

### Open Call Log

The Call Log application opens.

### Open Gallery

The Gallery or image picker opens.

### Set Alarm

The Alarm application opens with the selected alarm details.

### Open Camera

The Camera application opens.

### Open Login Activity

The Login Activity opens inside the application.

---

## 🧪 Testing

The application can be tested using the following operations:

| Test Case                 | Expected Result                       |
| ------------------------- | ------------------------------------- |
| Click Make Call           | Phone call action is launched         |
| Click Open URL            | Browser opens the specified URL       |
| Click Open Call Log       | Call Log opens                        |
| Click Open Gallery        | Gallery or image picker opens         |
| Click Set Alarm           | Alarm application opens               |
| Click Open Camera         | Camera application opens              |
| Click Open Login Activity | Login Activity opens                  |
| Deny permission           | Application handles permission denial |
| Grant permission          | Required operation can continue       |
| Check UI                  | Buttons are displayed correctly       |

---

## 🛠️ Troubleshooting

### 1. Application Crashes When Making a Call

Check that:

* `CALL_PHONE` permission is declared.
* Runtime permission is granted.
* The phone number is valid.
* The device supports phone calls.

---

### 2. URL Does Not Open

Check that:

* The URL starts with `https://`.
* `Intent.ACTION_VIEW` is used.
* `Uri.parse()` is used correctly.
* A suitable browser is installed.

---

### 3. Gallery Does Not Open

Check that:

* `Intent.ACTION_PICK` or `GetContent()` is used.
* The MIME type is `"image/*"`.
* The Activity result is handled correctly.

---

### 4. Camera Does Not Open

Check that:

* The device has a Camera application.
* The correct Intent action is used.
* Camera permission is handled if required.

---

### 5. Login Activity Does Not Open

Check that:

* `LoginActivity` exists.
* `LoginActivity` is registered in the Manifest.
* The package name is correct.
* The Explicit Intent is correct.

---

### 6. Permission Error

Check that:

* Permission is declared in `AndroidManifest.xml`.
* Runtime permission is requested when required.
* Permission result is handled correctly.

---

## 🎓 Study / Viva Questions

### 1. What is an Intent?

An Intent is a messaging object used to request an action from another Android component.

### 2. What are the types of Intent?

The two main types are **Implicit Intent** and **Explicit Intent**.

### 3. What is Implicit Intent?

Implicit Intent specifies an action without specifying the exact component.

### 4. What is Explicit Intent?

Explicit Intent specifies the exact Activity or component to be started.

### 5. What is Intent.setData()?

`setData()` sets the data URI of an Intent.

### 6. What is Intent.setType()?

`setType()` specifies the MIME type of the data.

### 7. What is Uri.parse()?

`Uri.parse()` converts a String into a URI object.

### 8. What is startActivity()?

`startActivity()` starts another Activity or performs an Intent action.

### 9. What is ACTION_CALL?

`ACTION_CALL` is used to make a phone call.

### 10. What is ACTION_VIEW?

`ACTION_VIEW` is used to view content such as URLs or other data.

### 11. What is ACTION_PICK?

`ACTION_PICK` is used to select an item from another application.

### 12. What is ACTION_SET_ALARM?

`ACTION_SET_ALARM` is used to open the Alarm application.

### 13. What is MediaStore.ACTION_IMAGE_CAPTURE?

It is used to request image capture from a Camera application.

### 14. What is `"image/*"`?

It is a MIME type that specifies image content.

### 15. What is `"tel:"`?

It is a URI scheme used to specify a telephone number.

### 16. What is CallLog.Calls.CONTENT_TYPE?

It is a constant representing the content type of Call Log data.

### 17. What is ActivityResultContracts?

ActivityResultContracts provides a modern way to launch Activities and receive results.

### 18. What is ContextCompat.checkSelfPermission()?

It checks whether a permission has been granted.

### 19. What is ActivityCompat.requestPermissions()?

It requests runtime permissions from the user.

### 20. What is ConstraintLayout?

ConstraintLayout is a layout used to position UI elements using constraints.

### 21. What is CoordinatorLayout?

CoordinatorLayout is a layout used to coordinate interactions between child views.

### 22. What is the difference between ACTION_CALL and ACTION_DIAL?

`ACTION_CALL` directly makes a call and requires the `CALL_PHONE` permission. `ACTION_DIAL` opens the dialer with the number filled in and lets the user press the call button.

### 23. What is the difference between ACTION_PICK and ACTION_GET_CONTENT?

Both can be used to select content. `ACTION_PICK` selects from a specific data source, while `ACTION_GET_CONTENT` allows the user to choose content from available applications.

### 24. Why are permissions required?

Permissions protect sensitive device features and user data.

### 25. Why is Explicit Intent used for Login Activity?

Because the application knows the exact Activity that needs to be opened.

---

## 📚 Learning Outcomes

After completing this practical, students will understand:

* How to create an Android application using Kotlin and XML.
* How to use Intent.
* How to use Implicit Intent.
* How to use Explicit Intent.
* How to use Intent Actions.
* How to use Intent.setData().
* How to use Intent.setType().
* How to use Uri.parse().
* How to use startActivity().
* How to make a call to a specific number.
* How to open a specific URL.
* How to open Call Log.
* How to open Gallery.
* How to set an Alarm.
* How to open Camera.
* How to open Login Activity.
* How to use ActivityResultContracts.
* How to check permissions.
* How to request permissions.
* How to use ConstraintLayout.
* How to use CoordinatorLayout.
* How to use Android system applications.

---

## ✅ Conclusion

This practical demonstrates the development of an **Android application using Kotlin and XML**.

The application uses **Implicit Intent** to perform operations such as making a call, opening a URL, viewing the Call Log, opening the Gallery, setting an Alarm, and opening the Camera.

It also uses **Explicit Intent** to open the Login Activity.

Through this practical, students learn how Android applications communicate with other components and applications using Intents.

---

## 👨‍💻 Author

**Yash Patel**

**Enrollment No.:** 25172022051

**Subject:** Mobile Application Development

---

## 📌 Repository

This project is available on GitHub:

**25172022051_MAD_PRACTICAL_3**

---

## 📄 License

This project is created for **educational and practical purposes**.
