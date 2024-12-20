# **Portfolio Tracker Application**

A simple web application to manage stock holdings, track their real-time value, and view portfolio metrics.

---

## **Features**
1. Add, view, edit, and delete stock holdings.
2. Dynamically calculate total portfolio value using real-time stock prices.
3. View portfolio distribution and top-performing stocks on the dashboard.

---

## **Steps to Run the Project Locally**

### **Frontend:**
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

4. Open the app in your browser:
   - Navigate to `http://localhost:3000`.

---

### **Backend:**
1. Navigate to the backend folder:
   ```bash
   cd backend
   ```

2. Set up the database:
   - Install MySQL and create a database called `portfolio_tracker`.
   - Update the database credentials in `application.properties`.

3. Build and run the Spring Boot application:
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

4. Backend will run on `http://localhost:8080`.

---

### **Database Setup:**
1. Create the necessary tables:
   - Use the following schema for the `stocks` table:
     ```sql
     CREATE TABLE stocks (
         id INT AUTO_INCREMENT PRIMARY KEY,
         name VARCHAR(255),
         ticker VARCHAR(255),
         buy_price DECIMAL(10,2),
         current_price DECIMAL(10,2)
     );
     ```
2. Populate initial data (optional).

---

### **Assumptions and Limitations**
1. **Real-Time Stock Prices:**
   - The app fetches stock prices from a free API (e.g., Alpha Vantage).
   - API rate limits may restrict frequent updates.

2. **Portfolio Composition:**
   - For simplicity, the quantity of each stock is assumed to be 1.

3. **Stock List:**
   - The app currently supports adding custom stocks but doesn’t validate ticker symbols.

4. **Editing Stocks:**
   - Stock details can be updated, but historical data isn't maintained.

---

### **Future Enhancements**
- Add user authentication to manage multiple portfolios.
- Validate ticker symbols using API data.
- Include historical performance graphs. 
