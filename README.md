# Hello App

A simple Python web application built with Flask that displays a welcome message.

## Features

- Simple Flask web server
- Welcome message endpoint
- Ready for local development and testing

## Prerequisites

Before running this application, make sure you have the following installed:

- **Python 3.8 or higher** (Python 3.12 recommended)
- **pip** (Python package installer)

## Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/sanjithdevineni/hello-app.git
cd hello-app
```

### 2. Create a Virtual Environment

It's recommended to use a virtual environment to isolate project dependencies:

```bash
# Create a virtual environment
python3 -m venv venv

# Activate the virtual environment
# On macOS/Linux:
source venv/bin/activate

# On Windows:
# venv\Scripts\activate
```

### 3. Install Dependencies

With your virtual environment activated, install the required packages:

```bash
pip install -r requirements.txt
```

This will install:
- Flask==2.0.2
- Werkzeug==2.0.3 (compatible version)

## Running the Application

### Local Development

1. **Start the Flask server:**
   ```bash
   python main.py
   ```

2. **Access the application:**
   Open your web browser and navigate to:
   ```
   http://127.0.0.1:8080
   ```
   
   You should see the message: "Congratulations, it's a web app!"

### Application Details

- **Host:** 127.0.0.1 (localhost)
- **Port:** 8080
- **Debug Mode:** Enabled (auto-reloads on code changes)

## Project Structure

```
hello-app/
├── main.py              # Main Flask application
├── requirements.txt     # Python dependencies
├── app.yaml            # App configuration
├── README.md           # This file
├── .gitignore          # Git ignore rules
└── venv/               # Virtual environment (not in git)
```

## Development

### Making Changes

1. Edit `main.py` to modify the application
2. The server will automatically reload when you save changes (debug mode is enabled)
3. Refresh your browser to see the changes

### Adding New Routes

To add new endpoints, modify `main.py`:

```python
@app.route('/new-route')
def new_route():
    return "This is a new route!"
```

## Troubleshooting

### Common Issues

1. **Port already in use:**
   - Change the port in `main.py` from 8080 to another port (e.g., 5000, 8000)
   - Or kill the process using the current port

2. **Import errors:**
   - Make sure your virtual environment is activated
   - Reinstall dependencies: `pip install -r requirements.txt`

3. **Permission errors:**
   - On macOS/Linux, you might need to use `python3` instead of `python`

### Checking Installation

Verify that Flask is installed correctly:

```bash
python -c "import flask; print(flask.__version__)"
```

## Deployment

This application is configured for Google App Engine deployment with the included `app.yaml` file.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test locally
5. Submit a pull request
