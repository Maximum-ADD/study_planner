# study_planner
This is an app we want to build so that we have some sort of project under our belt that is not owned by Wits University. It will schedule study sessions from a user's subject list, stated study preference, focus list, and user provided test dates. The user should then be able to edit their schedule and save it as a pdf or other file.



**React Native Setup Guide (Basic Use Only)**
For teammates who need to download, open, and run a React Native app without building it from scratch.

---

**1. Install Node.js**

* Go to: [https://nodejs.org](https://nodejs.org)
* Download the **LTS version (.msi)**
* Install with default settings (ensure npm is included)
* Confirm installation in terminal:

  ```bash
  node -v  
  npm -v
  ```

---

**2. Install Java Development Kit (JDK)**

* Go to: [https://adoptium.net](https://adoptium.net)
* Download **Temurin OpenJDK 17 MSI**
* Install with default settings
* Confirm:

  ```bash
  java -version  
  javac -version
  ```

---

**3. Install Android Studio**

* Download from: [https://developer.android.com/studio](https://developer.android.com/studio)
* During install, select:

  * Android SDK
  * Android SDK Platform
  * Android Virtual Device (AVD)
* Open Android Studio → AVD Manager → Create and launch emulator

---

**4. Set up Environment Variables**
Add this to `.bashrc`, `.zshrc`, or Windows `Environment Variables`:

```sh
ANDROID_HOME=<your SDK path>
# Typically: C:\Users\<YourUser>\AppData\Local\Android\Sdk

Add to PATH:
%ANDROID_HOME%\platform-tools
%ANDROID_HOME%\emulator
```

---

**5. Clone or Receive the React Native App Folder**

* Download project folder from GitHub or shared drive
* Open it in **Visual Studio Code** or any editor

---

**6. Install App Dependencies**
Open terminal inside the project folder:

```bash
npm install
```

---

**7. Start Android Emulator**

* Open Android Studio → AVD Manager → Launch a virtual device
  OR

```bash
emulator -avd <your_device_name>
```

---

**8. Run the App**
Inside project folder:

```bash
npx react-native run-android
```

---

**9. Make Edits (Optional)**

* Open `App.js` in VS Code
* Change UI or logic
* Save and re-run app to see updates

---

**10. Troubleshooting**

* If `npm` fails in PowerShell, use Command Prompt (`cmd.exe`)
* Restart terminal after installing Node or JDK
* Ensure emulator is running before `npx react-native run-android`

Done. They can now open, edit, and run a React Native app.






 This is for Adrian who is setting up the app:
**React Native Setup (from zero)**

1. **Install Node.js**

   * Download and install: [https://nodejs.org](https://nodejs.org)
   * Confirms `node -v` and `npm -v` work in terminal.

2. **Install Java JDK (11 or higher)**

   * Download: [https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)
   * Set environment variable `JAVA_HOME` to JDK path.

3. **Install Android Studio**

   * Install from: [https://developer.android.com/studio](https://developer.android.com/studio)
   * During setup, select:

     * Android SDK
     * Android SDK Platform
     * Android Virtual Device (AVD)
   * In Android Studio:

     * Open **SDK Manager**
     * Enable SDK Tools: "Android SDK Command-line Tools"
     * Open **AVD Manager**, create a virtual device (e.g., Pixel 4 API 33)

4. **Set environment variables**
   Add these to your shell config (`.bashrc`, `.zshrc`, `.profile`):

   ```sh
   export ANDROID_HOME=$HOME/Library/Android/sdk
   export PATH=$PATH:$ANDROID_HOME/emulator
   export PATH=$PATH:$ANDROID_HOME/platform-tools
   ```

5. **Install React Native CLI**

   ```bash
   npm install -g react-native-cli
   ```

6. **Create your app**

   ```bash
   npx react-native init StudyPlanner
   cd StudyPlanner
   ```

7. **Run Android emulator**

   * Open Android Studio → AVD Manager → Launch device
     OR

   ```bash
   emulator -avd <your_emulator_name>
   ```

8. **Start the app**

   ```bash
   npx react-native run-android
   ```

9. **Edit `App.js`**

   ```js
   import React from 'react';
   import { View, Text } from 'react-native';

   const App = () => (
     <View>
       <Text>Study Planner</Text>
     </View>
   );

   export default App;
   ```

10. **Use VS Code for development**

* Download: [https://code.visualstudio.com](https://code.visualstudio.com)
* Open folder: `StudyPlanner`
* Install extensions:

  * React Native Tools
  * JavaScript / TypeScript

Done. Full React Native environment with emulator.
