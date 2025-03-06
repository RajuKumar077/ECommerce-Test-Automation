## 🚀 **E-Commerce Order Placement Automation (Selenium + Cucumber)**  

### 📌 **Project Overview**  
This project automates the end-to-end process of placing an order on an e-commerce website using **Selenium WebDriver, Cucumber BDD, and JUnit**. The framework follows the **Page Object Model (POM)** for better maintainability and scalability.  

---

## 📂 **Project Structure**  

### 🔹 1. **Feature Files (BDD Scenarios)**
- Location: `src/test/resources/features/`
- File: `Placeorder.feature`
- Contains the **Gherkin syntax** defining test scenarios for placing an order.  
- Uses `Examples` table to pass **dynamic login credentials and user details**.  

### 🔹 2. **Step Definitions**  
- Location: `src/test/java/stepDefinition/`
- File: `PlaceOrderStepDef.java`
- Maps **Gherkin steps** from `Placeorder.feature` to actual Selenium WebDriver actions.  

### 🔹 3. **Page Object Model (POM) Classes**  
- Location: `src/test/java/pages/`
- Includes:
  - `LoginPage.java` → Handles login functionality.
  - `ProductListPage.java` → Selects a product.
  - `CartPage.java` → Adds items to the cart.
  - `CheckoutPage.java` → Proceeds to checkout.
  - `CustomerInfoPage.java` → **Now dynamically fills customer details using Examples table.**
  - `LogOffPage.java` → Logs out the user.

### 🔹 4. **Locators & Utilities**
- Location: `src/test/java/objectrepository/`
- File: `Locators.java`
- Stores **XPath/CSS selectors** for elements.  

- Location: `src/test/java/utils/`
- Files:
  - `Base.java` → WebDriver setup.
  - `Reporter.java` → Generates **Extent Reports** for test execution.

---

## 📖 **How It Works**
### ✅ **1. Login**  
- Uses the **Examples table** to enter different `UserName` and `Password`.  
- Authenticates the user using `LoginPage.java`.  

### ✅ **2. Product Selection & Cart**  
- Selects an item from `ProductListPage.java`.  
- Adds it to the cart using `CartPage.java`.  
- Proceeds to checkout via `CheckoutPage.java`.  

### ✅ **3. Customer Info (Dynamic Input)**  
- **Dynamically fills** user details (First Name, Last Name, Postal Code) from the Examples table.  
- Handled in `CustomerInfoPage.java`.  

### ✅ **4. Order Placement & Logout**  
- Verifies order details & completes checkout.  
- Logs out the user using `LogOffPage.java`.  

---

## 🔍 **Where to Learn More?**  
Want to understand the technologies used? Check out these resources:  

- **Selenium WebDriver**: [Selenium Docs](https://www.selenium.dev/documentation/)  
- **Cucumber BDD**: [Cucumber Docs](https://cucumber.io/docs/)  
- **JUnit Testing**: [JUnit Docs](https://junit.org/)  
- **Page Object Model (POM)**: [POM Explanation](https://www.toolsqa.com/selenium-webdriver/page-object-model/)  
- **Extent Reports**: [Extent Report Guide](https://www.extentreports.com/)  

---

## 🛠 **How to Run the Tests?**
1. Clone the repository  
   ```bash
   git clone <repository-url>
   cd <project-folder>
   ```
2. Install dependencies  
   - Ensure **Java, Maven, and Selenium dependencies** are set up.  
3. Run the tests  
   ```bash
   mvn test
   ```
4. View reports in `test-output/`  

---

## 📌 **Final Notes**
This framework is designed for **scalability and maintainability**, making it easy to test different scenarios by updating the **Examples table** in `Placeorder.feature`.  

---
