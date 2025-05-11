# Hospital Management System (HMS)

## Overview

This **Hospital Management System (HMS)** is designed to manage hospital processes like patient registration, appointment scheduling, doctor management, and displaying available services. The project is built using **Python** with **Tkinter** for the GUI and **MySQL** as the database backend.

## Features

- **Patient Registration**: Allows users to register with personal details (like Aadhar card, name, age, gender, phone number, blood group).
- **Appointment Scheduling**: Allows patients to book appointments with doctors, view available services, and generate appointment details.
- **Doctor List**: Displays a list of doctors and their specialties.
- **Service Availability**: Shows available services like X-ray, Ultrasound, MRI, etc., along with their room numbers.
- **Data Modification**: Enables modification of patient details based on their Aadhar card number.
- **Data Viewing**: Displays patient data for a given Aadhar card number.
- **Interactive UI**: The system uses Tkinter to provide a user-friendly graphical interface.

## Technologies Used

- **Python**: The main language for developing the application.
- **Tkinter**: For the graphical user interface.
- **MySQL**: For database management.
- **Random**: To generate random appointment numbers and doctor choices.

## Installation

1. **Clone the repository**:

    ```bash
    git clone https://github.com/your-username/hms.git
    cd hms
    ```

2. **Install MySQL**:
   - Make sure you have MySQL installed and running on your system.
   - Create a database called `Hospital`.

3. **Set up the MySQL Database**:
   - You need to create the tables in MySQL for patient registration and appointment details.
   - Below are the SQL statements to set up the database and tables.

    ```sql
    CREATE DATABASE IF NOT EXISTS Hospital;

    USE Hospital;

    CREATE TABLE IF NOT EXISTS appointment (
        idno VARCHAR(12) PRIMARY KEY,
        name CHAR(50),
        age CHAR(3),
        gender CHAR(1),
        phone VARCHAR(10),
        bg VARCHAR(3)
    );

    CREATE TABLE IF NOT EXISTS appointment_details (
        idno VARCHAR(12) PRIMARY KEY,
        doctor VARCHAR(50),
        date VARCHAR(20),
        time VARCHAR(20),
        appointment_no VARCHAR(10)
    );
    ```

4. **Install Python Dependencies**:
   Ensure you have Python installed (preferably Python 3.x).

   - Install the necessary Python packages using pip (if you haven’t already):

     ```bash
     pip install mysql-connector tkinter
     ```

## Usage

### Main Menu
The main menu of the application provides buttons for various actions:

1. **Registration**: To register a new patient with personal details.
2. **Appointment**: To book an appointment by providing the Aadhar number and other details.
3. **List of Doctors**: To view the list of doctors available in different departments.
4. **Services Available**: To see available hospital services (X-ray, Ultrasound, etc.).
5. **View Data**: To view the registered patient details using Aadhar number.
6. **Modify Existing Data**: To modify patient details (name, age, gender, phone number, blood group).
7. **Exit**: Closes the application.

### How to Register a Patient

1. Click the **"Registration"** button from the main menu.
2. Enter the **Aadhar card number**, **name**, **age**, **gender**, **phone number**, and **blood group**.
3. After clicking **Submit**, the system will display a success message confirming the registration.

### How to Book an Appointment

1. Click the **"Appointment"** button from the main menu.
2. Enter the **Aadhar number** of the registered patient.
3. Select the **department** and enter the **appointment date** and **time**.
4. The system will generate an appointment number and display the doctor assigned along with the appointment details.

### How to Modify Data

1. Click the **"Modify Existing Data"** button from the main menu.
2. Enter the **Aadhar number** of the patient whose details need to be modified.
3. Choose which field to modify (name, age, gender, phone, or blood group).
4. Enter the new details and click **Submit**.

### How to View Patient Data

1. Click the **"View Data"** button from the main menu.
2. Enter the **Aadhar number** to view the patient's registered details.

## Contributing

We welcome contributions! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-name`).
6. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or suggestions, feel free to reach out:

- Email: prasadkolusu09@gmail.com 
- GitHub: [Your GitHub](https://github.com/Sateesh939852)
