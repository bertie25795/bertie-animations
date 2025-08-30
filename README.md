## Project's Title
**Bertie: Bluetooth Bloodhound** is an innovative web application designed to help users quickly and easily locate their misplaced Bluetooth-enabled hearing aids using an intuitive directional compass, dynamic visual cues, and helpful audio/haptic feedback.

## Project Description
Losing a small, essential device like a hearing aid can be incredibly stressful. Bertie aims to alleviate this common problem by leveraging proximity-sensing technology to guide users directly to their lost devices. 
Built on the Base44 platform, this application provides a modern, responsive, and engaging user experience.

### What the application does:
*   **Device Management:** Allows users to "pair" (simulate adding) their hearing aids, view their details, and manage active tracking status.
*   **Intuitive Locator:** Features a dynamic compass interface where "Bertie the Bloodhound" points the way, visually indicating the direction and proximity to the lost device.
*   **Multi-Sensory Feedback:** Provides simulated signal strength indicators, distance estimations, and optional audio "barks" (using the Web Audio API) and vibration feedback to assist in the search.
*   **Last Known Location Map:** Displays the last recorded location of a hearing aid on a map, offering a starting point for the search.
*   **User Preferences:** Customizable accessibility settings for audio, vibration, visual-only mode, and font scaling.
*   **App Unlock Mechanism:** Integrates a simulated purchase restoration and promo code redemption system to manage app access.
*   **Promotional Tools:** Includes a simple interface for generating unique promotional codes for marketing or partner initiatives.

### Why the technologies were used:
The application is developed on the **Base44 platform**, which provides robust infrastructure for user management, authentication, data persistence (entities), and deployment. 
This allowed us to focus primarily on the core business logic and user experience rather than backend complexities.

*   **React:** For building a dynamic and responsive user interface.
*   **Tailwind CSS & Shadcn/UI:** For a modern, clean, and highly customizable design system, ensuring a polished look and feel.
*   **Lottie Animations:** To bring "Bertie" to life with smooth, scalable vector animations, making the tracking experience more engaging and visually appealing.
*   **Web Audio API:** For programmatic sound generation (the "barks") to provide immediate audio feedback without relying on pre-recorded sound files.

### Challenges faced and future features:
*   **Bluetooth Integration Simulation:** As direct native Bluetooth API access is limited in a web app context (and specifically within the Base44 environment for this project's scope),
*   the application utilizes mock data and simulated RSSI readings to demonstrate core functionality. A future enhancement would be direct, native Bluetooth integration for real-world tracking.
*   **Lottie Animation Integration:** Integrating Lottie animations required careful coordination with the Base44 platform's specific methods for injecting global JavaScript libraries (like `lottie-web`) and hosting external static assets (Lottie JSON files on GitHub Pages).
*   This process highlighted the importance of understanding the platform's unique deployment mechanisms.
*   **Precise Directionality:** While the compass provides a heading, achieving pinpoint directional accuracy in a web environment using standard Bluetooth APIs for consumer devices can be challenging.
*   Future iterations could explore advanced techniques or hardware integrations for enhanced precision.

## Table of Contents
1.  [Project's Title](#-bertie-bluetooth-bloodhound-)
2.  [Project Description](#project-description)
3.  [Installation and Running the Project](#installation-and-running-the-project)
4.  [How to Use the Project](#how-to-use-the-project)
    *   [Main Screens Overview](#main-screens-overview)
    *   [App Unlock](#app-unlock)
    *   [Tracking Your Device](#tracking-your-device)
    *   [Managing Devices](#managing-devices)
    *   [Viewing Last Location](#viewing-last-location)
    *   [Adjusting Settings](#adjusting-settings)
5.  [Credits](#credits)
6.  [License](#license)

## Installation and Running the Project
This application is built and deployed on the Base44 platform. Therefore, it is not designed for traditional local installation via `npm install` and `npm start`.

To experience the application:
1.  **Access the Live App:** The app is typically hosted directly on a Base44 URL. Please refer to the project owner for the live deployment link.
2.  **Base44 Development Environment:** For development and modification, the project lives within the Base44 builder interface, where changes are applied and previewed in real-time.

**Dependencies:**
*   **Base44 Platform:** The primary hosting and development environment.
*   **External Lottie Animations:** JSON files for Bertie's animations are hosted externally on GitHub Pages (e.g., `https://bertie25795.github.io/bertie-animations/`).
*   **Lottie Web Player:** The `lottie.min.js` script is injected globally into the application via Base44's custom script injection feature to enable Lottie animation playback.

## How to Use the Project

### Main Screens Overview
Here are some screenshots showcasing the application's key interfaces:

*   **Locator Screen (Compass View):**
    ![Screenshot of Locator Screen]
    <img width="995" height="784" alt="Screenshot 2025-08-30 19 07 05" src="https://github.com/user-attachments/assets/a3faae51-83da-49cb-a2ec-50e60decdf6f" />


*   **Devices Management:**
    ![Screenshot of Devices Screen]
   <img width="995" height="784" alt="image" src="https://github.com/user-attachments/assets/ad24cd08-24f3-4838-ae88-123034633ae6" />


*   **Last Known Location Map:**
    ![Screenshot of Map View]
    <img width="995" height="784" alt="image" src="https://github.com/user-attachments/assets/b4bd1166-4f7b-41f3-bb6d-5a1098f84c3b" />


*   **Settings Screen:**
    ![Screenshot of Settings Screen]
    <img width="995" height="784" alt="image" src="https://github.com/user-attachments/assets/a43890c9-ce67-40dd-b1c2-d526e14c9d5b" />


### App Unlock
Upon first access, the app will require unlocking. You can either:
*   **Restore Purchase:** (Simulated) Click the "Restore Purchase" button if you've previously "purchased" the app.
*   **Enter Promo Code:** Input a valid promo code and click "Apply."
    *   *Example Promo Code (for testing/development purposes, if applicable):* `BLOODHOUND-ABCXYZ` (Replace with an actual code generated from the Promo Website page, if you have one setup).

### Tracking Your Device
1.  Navigate to the **Locator** page.
2.  Select a paired hearing aid from the "Paired Devices" dropdown.
3.  Click "Start Tracking."
4.  Observe Bertie's direction and the signal strength indicator. Listen for audio cues (barks!) and feel for vibrations as you move around.
5.  Bertie will guide you closer to your device.

### Managing Devices
1.  Go to the **Devices** page.
2.  Here you can see all your "paired" hearing aids.
3.  Click "Add Device" to simulate scanning for and pairing a new hearing aid.
4.  For existing devices, you can activate/deactivate them or remove them from your list.

### Viewing Last Location
1.  Visit the **Map View** page.
2.  Select a hearing aid from the dropdown.
3.  The map will display the last recorded location of that device.
4.  Click "Navigate to Location" to open the location in your device's default map application (e.g., Google Maps).

### Adjusting Settings
1.  Access the **Settings** page.
2.  Here you can:
    *   View your account information.
    *   Sign out.
    *   Customize accessibility preferences: toggle audio feedback, vibration feedback, visual-only mode, and adjust the global font scale.
    *   View app version information and access links to privacy policy/terms (placeholders).

## Credits
This project was developed with contributions from:

*   **Siobhan Wilson/GitHub bertie25795]** - Primary Developer
*   **AI Assistant (Base44)** - For code generation, architectural guidance, and debugging.

Special thanks to the Base44 support team for their assistance with platform-specific configurations.

## License
This project is licensed under the **MIT License**.

Feel free to use, modify, and distribute this project as per the terms of the MIT License.
