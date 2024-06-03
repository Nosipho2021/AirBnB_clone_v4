0x06. AirBnB clone - Web dynamic
Python
Front-end
JavaScript

## Project Overview
AirBnB Clone v4 is an enhanced version of the AirBnB clone project. This project includes dynamic web features using Flask for the backend and JavaScript with jQuery for the frontend. The application allows users to search for and filter places to stay, mimicking the functionality of the AirBnB website.

## Features
- Dynamic content loading without page reloads
- Interactive filters for amenities
- API status indicator
- Fetch and display places dynamically
- Real-time filtering based on selected amenities

## Setup Instructions
### Prerequisites
- Python 3.x
- Flask
- jQuery 3.2.1

### Installation
1. **Clone the Repository**
    ```bash
    git clone https://github.com/yourusername/AirBnB_clone_v4.git
    cd AirBnB_clone_v4
    ```

2. **Install Required Dependencies**
    ```bash
    sudo apt-get install -y python3-lxml
    sudo pip3 install flask_cors flasgger
    ```

3. **Troubleshoot Dependencies**
    - If you encounter a `jsonschema` exception:
        ```bash
        sudo pip3 uninstall -y jsonschema 
        sudo pip3 install jsonschema==3.0.1
        ```
    - If you see `No module named 'pathlib2'`:
        ```bash
        sudo pip3 install pathlib2
        ```

4. **Expose Ports in Vagrantfile**
    - Add the following line to your `Vagrantfile` to forward port 5001:
        ```ruby
        config.vm.network :forwarded_port, guest: 5001, host: 5001
        ```

### Starting the Application
1. **Run the Flask Application**
    ```bash
    HBNB_MYSQL_USER=hbnb_dev HBNB_MYSQL_PWD=hbnb_dev_pwd HBNB_MYSQL_HOST=localhost HBNB_MYSQL_DB=hbnb_dev_db HBNB_TYPE_STORAGE=db python3 -m web_dynamic.0-hbnb
    ```

2. **Start the API on Port 5001**
    ```bash
    HBNB_MYSQL_USER=hbnb_dev HBNB_MYSQL_PWD=hbnb_dev_pwd HBNB_MYSQL_HOST=localhost HBNB_MYSQL_DB=hbnb_dev_db HBNB_TYPE_STORAGE=db HBNB_API_PORT=5001 python3 -m api.v1.app
    ```

## Usage
- **Search for Listings**: Users can search for listings and view detailed information.
- **Filter by Amenities**: Users can select amenities to filter the listings dynamically.
- **API Status Check**: The application indicates the status of the API.

## Contributor 
- Nosipho Mdakane
