<div align="center">
    <h1> <img src="YOUR_LOGO_URL_HERE" width="80px"><br/>Passwordless Authentication</h1>
</div>
<p align="center"> <a href="https://github.com/default-cybe" target="_blank"><img alt="" src="https://img.shields.io/badge/Website-EA4C89?style=normal&logo=dribbble&logoColor=white" style="vertical-align:center" /></a> <a href="https://twitter.com/default_yt_" target="_blank"><img alt="" src="https://img.shields.io/badge/Twitter-1DA1F2?style=normal&logo=twitter&logoColor=white" style="vertical-align:center" /></a> <a href="https://www.instagram.com/kaivalya_ahir" target="_blank"><img alt="" src="https://img.shields.io/badge/Instagram-E4405F?style=normal&logo=instagram&logoColor=white" style="vertical-align:center" /></a> <a href="https://www.linkedin.com/in/kaivalya-ahir/" target="_blank"><img alt="" src="https://img.shields.io/badge/LinkedIn-0077B5?style=normal&logo=linkedin&logoColor=white" style="vertical-align:center" /></a> </p>

# Passwordless Authentication

This project implements a passwordless authentication system, providing a secure and user-friendly login experience. By leveraging various factors such as cookies, location, IP address, device fingerprint, and browsing history, the system dynamically calculates a trust score. Based on this score, users are granted access or prompted for additional verification, like two-factor authentication, ensuring robust security without the need for traditional passwords.

# Description

Passwordless-auth allows users to log in without entering a password. It utilizes a sophisticated trust score system to determine the legitimacy of a login attempt. This system enhances security by minimizing the risk of password-related breaches while improving user convenience.

# Features

* **Passwordless Login:** Eliminate the need for traditional passwords.
* **Trust Score System:** Utilizes cookies, location, IP address, device fingerprint, and history to calculate a dynamic trust score.
* **Adaptive Security:** Requires two-factor authentication or other verification methods when the trust score is insufficient.
* **Enhanced Security:** Reduces the risk of password-related vulnerabilities.
* **Improved User Experience:** Streamlines the login process for a seamless experience.

# Tech Used

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![Bootstrap](https://img.shields.io/badge/bootstrap-%23563D7C.svg?style=for-the-badge&logo=bootstrap&logoColor=white) ![Any other technologies used here]

# Installation

To set up and run this project, follow these steps:

**Note: Ensure you have Python and Django installed on your system.**

1.  **Create a Virtual Environment:**
    ```bash
    python -m venv myvenv
    ```

2.  **Activate the Virtual Environment:**
    * **Windows:**
        ```bash
        myvenv\Scripts\activate
        ```
    * **macOS/Linux:**
        ```bash
        source myvenv/bin/activate
        ```

3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    (Ensure `requirements.txt` is in your project directory.)

4.  **Run the Development Server:**
    ```bash
    python manage.py runserver
    ```

5.  **Configuration:**
    * Configure any necessary settings, such as database connections or API keys, in your Django project's `settings.py` file.
    * If you have any specific configuration regarding the trust score system, adjust the code accordingly.

6.  **Access the Application:**
    * Open your web browser and navigate to `http://127.0.0.1:8000/` to access the application.
