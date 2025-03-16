# **Get Rid of Boring**

A simple and interactive web application that generates engaging activities for users when they're feeling bored. By integrating with the **Bored API**, users can filter activities based on type and the number of participants to find something fun and exciting to do.

---

## **Features**
- **Random Activity Generator**:
  - Fetches a random activity suggestion from the Bored API.
- **Activity Filtering**:
  - Allows users to filter activities by type (e.g., education, recreational, relaxation) and number of participants.
- **Dynamic Feedback**:
  - Displays the generated activity details directly on the page.
- **Error Handling**:
  - Provides meaningful error messages when no activity matches the specified criteria.

---

## **Technologies Used**
- **Node.js**: Backend runtime environment for managing server-side logic.
- **Express.js**: Framework for creating server routes and handling requests.
- **Axios**: Library for making HTTP requests to the Bored API.
- **EJS (Embedded JavaScript Templates)**: For rendering dynamic HTML pages.
- **CSS**: For styling the application and creating a responsive layout.
- **Bored API**: External API providing activity suggestions.

---

## **Getting Started**

### **Prerequisites**
- **Node.js**: Ensure that Node.js is installed on your system.

---

### **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/Ayu1404/Get-Rid-of-Boring.git
   cd Get-Rid-of-Boring
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the server:
   ```bash
   node app.js
   ```

4. Open your browser and navigate to:
   ```plaintext
   http://localhost:7001
   ```

---

## **How to Use**
1. **Access the App**:
   - Open the web app in your browser at `http://localhost:7001`.
2. **Generate a Random Activity**:
   - Leave all fields empty and click **Go** to get a random activity suggestion.
3. **Filter Activities**:
   - Select an activity type and/or the number of participants from the dropdown menus.
   - Click **Go** to get activities matching the selected criteria.
4. **View Results**:
   - The activity name, type, and number of participants will be displayed dynamically.
5. **Error Handling**:
   - If no activity matches the criteria, an error message is displayed on the page.

---

## **File Structure**
### **Backend (app.js)**:
- **Endpoints**:
  - **GET `/`**:
    - Fetches and displays a random activity from the Bored API.
  - **POST `/`**:
    - Fetches and displays filtered activities based on user input.
- **API Integration**:
  - Communicates with the Bored API to retrieve activity suggestions.
- **Error Handling**:
  - Handles failed requests and displays error messages in the interface.

### **Front-End (solution.ejs)**:
- **Form-Based Filtering**:
  - Users can select activity type and participant count from dropdown menus.
- **Dynamic Content Display**:
  - Shows activity suggestions or error messages based on API responses.

---

## **Project Highlights**
- **Activity Types**:
  - Education
  - Charity
  - Recreational
  - Relaxation
  - Busywork
  - Social
  - DIY
  - Music
- **Participants**:
  - Filter activities for 1 to 4 participants, or choose "Any number of people."

---

## **Sample API Interaction**
### **Random Activity (Default GET Request)**:
- **Endpoint**:
  ```plaintext
  https://bored-api.appbrewery.com/random
  ```
- **Example Response**:
  ```json
  {
    "activity": "Learn how to fold a paper crane",
    "type": "education",
    "participants": 1
  }
  ```

### **Filtered Activity (POST Request)**:
- **Endpoint**:
  ```plaintext
  https://bored-api.appbrewery.com/filter?type={type}&participants={participants}
  ```
- **Example Query**:
  ```plaintext
  type=diy&participants=2
  ```
- **Example Response**:
  ```json
  [
    {
      "activity": "Build a birdhouse",
      "type": "diy",
      "participants": 2
    }
  ]
  ```

---

## **Contributing**
Contributions are welcome! To contribute:
1. Fork this repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

---

## **License**
This project is licensed under the MIT License, allowing you to modify and distribute the project with proper attribution.

---

## **Acknowledgments**
- Thanks to the **Bored API** for providing an excellent resource for activity suggestions.
- Inspired by the need to make life a little less boring!
