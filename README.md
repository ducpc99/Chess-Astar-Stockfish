# ChessWeb Project

## How to Run the Local Server

1. **Open a Terminal**: Navigate to the project directory where you want to run the server.

2. **Install Dependencies**: 
   - Ensure you have Python and `pip` installed. Use the following command to install the dependencies listed in `requirements.txt`:
     ```bash
     pip install -r requirements.txt
     ```
   - If the installation encounters issues, you can manually install the required dependencies:
     ```bash
     pip install asgiref==3.7.2 chess==1.10.0 Django==4.2.6 psycopg2-binary==2.9.9 sqlparse==0.4.4 typing_extensions==4.8.0 stockfish
     ```

3. **Run the Server**:
   - From the root directory of the project, start the server using:
     ```bash
     python manage.py runserver
     ```

## Basic Structure of the Web Application

![Chess Game](./static/image.png)

- **`ChessWeb/chessWeb`**: This directory contains files for managing and deploying the web application.
  
- **Static Files**: The `static` folder holds static files such as images, CSS, and JavaScript. 
  - **`chess.js`**: This file is the most important in this folder, containing the main logic for the chessboard and using AJAX to send and receive data between the web interface and the algorithm in `users/views.py`.

### Important Directories and Files in `users`:

- **`users/templates`**: Contains HTML files used to create and edit web objects.

- **`users/views.py`**: Handles the communication (data transmission and reception) between the frontend and the Python algorithms.

- **`users/urls.py`**: Imports functions from `views.py` for execution.

- **`users/stockfish.py`**: Interfaces with the Stockfish open-source chess engine.

- **`users/algorithms.py`**: Contains the Alpha-Beta pruning algorithm.

## Additional Information

The project includes other files necessary for setting up a complete Django web application, but the components listed above are the most important.
