## Expo iOS Project Setup Guide
Always select For learning with Expo Go (SDK 54) from the terminal menu. The absolute latest versions can cause strict Swift/Xcode compilation errors and dependency mismatches.

##  Step 1: Initialize the Project (In an Existing Folder)
Make sure your target folder is completely empty. Navigate into it and run:

npx create-expo-app@latest .

When prompted by the interactive terminal menu, use your arrow keys to select SDK 54 and press Enter.

## Step 2: Prepare Your Physical iPhone
Before running the build command, configure your iOS device:

   1. Connect your iPhone to your Mac using a USB cable (required for the initial build only).
   2. Unlock your iPhone and tap "Trust This Computer" when prompted.
   3. On your iPhone, go to Settings > Privacy & Security > Developer Mode and turn it ON (requires a phone restart).
   4. Ensure both your Mac and iPhone are connected to the exact same Wi-Fi network.

## Step 3: Build and Install on Your Device
Run the native iOS build command to compile the app and install it directly onto your connected iPhone:

npx expo run:ios --device

Select your physical iPhone from the terminal list. Once this process finishes, the app icon will appear on your iPhone home screen.

## Step 4: Daily Wireless Coding
After this initial installation is successful, you no longer need the USB cable.
For everyday development, simply keep both devices on the same Wi-Fi network and run:

npx expo run:ios --device

Open the installed app on your phone, and it will instantly load your code changes wirelessly.


------------------------------
## Multi-Language Naming Conventions

## Frontend (React Native / Expo / TypeScript)

* Folders & Files: Use kebab-case (e.g., user-profile/card-component.tsx).
* Functions & Classes: Use PascalCase (e.g., function UserProfile(), class AuthManager).
* React Hooks: Use camelCase prefixed with "use" (e.g., const useCustomState = () => {}).
* Suggestion: Use camelCase for regular TypeScript utility variables and helper functions that are not React components or hooks (e.g., const formatCurrency = () => {}).

## Backend (Go)

* Folders & Files: Use lowercase snake_case or flat lowercase for files, and flat lowercase for packages.
* Correction: Go officially discourages kebab-case because dashes are illegal in package names. Use user_profile.go
* Functions, Structs, & Interfaces: Use PascalCase for exported items, and camelCase for unexported (private) items.
* Example: type User struct {} (public) vs type user struct {} (private).

## Backend (Python)

* Folders: Use kebab-case (e.g., user-service/).
* Files / Modules: Use snake_case (e.g., auth_middleware.py).
* Classes: Use PascalCase (e.g., class DatabaseConnection:).
* Functions & Methods: Use snake_case (e.g., def calculate_total():).


