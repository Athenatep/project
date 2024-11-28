# Email Validator Installation Guide

## Prerequisites

1. **Python 3.9 or higher**
   ```bash
   python --version  # Check Python version
   ```

2. **Git**
   ```bash
   git --version  # Check Git version
   ```

3. **Node.js 18 or higher**
   ```bash
   node --version  # Check Node.js version
   ```

## Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/email-validator.git
   cd email-validator
   ```

2. **Create Python Virtual Environment**
   ```bash
   python -m venv venv
   
   # On Windows
   .\venv\Scripts\activate
   
   # On Linux/macOS
   source venv/bin/activate
   ```

3. **Install Dependencies**
   ```bash
   # Install Python dependencies
   pip install -r requirements.txt
   
   # Install Node.js dependencies
   npm install
   ```

4. **Create Required Directories**
   ```bash
   mkdir -p logs
   mkdir -p reports/visualizations
   mkdir -p data
   ```

5. **Configure the Application**
   - Copy `config/config.example.json` to `config/config.json`
   - Update configuration settings as needed

## Running the Application

1. **Start the GUI Application**
   ```bash
   npm run start
   ```

2. **Start the REST API**
   ```bash
   npm run api
   ```

3. **Run Tests**
   ```bash
   npm test
   ```

## Development Setup

1. **Install Development Dependencies**
   ```bash
   pip install -r requirements-dev.txt
   ```

2. **Setup Pre-commit Hooks**
   ```bash
   pre-commit install
   ```

3. **Code Formatting**
   ```bash
   npm run format
   ```

4. **Linting**
   ```bash
   npm run lint
   ```

## Troubleshooting

### Common Issues

1. **Missing Qt Dependencies**
   
   On Ubuntu/Debian:
   ```bash
   sudo apt-get update
   sudo apt-get install python3-pyqt6
   ```

   On Windows:
   - Ensure Microsoft Visual C++ Redistributable is installed

2. **Permission Issues**
   ```bash
   # Fix directory permissions
   chmod -R 755 .
   ```

3. **Module Not Found Errors**
   - Ensure virtual environment is activated
   - Verify all dependencies are installed:
     ```bash
     pip freeze
     ```

4. **Port Already in Use**
   - Check if another instance is running
   - Change port in config.json

### Getting Help

- Check logs in `logs/email_validator.log`
- Open an issue on GitHub
- Contact support team

## Updating

1. **Update Repository**
   ```bash
   git pull origin main
   ```

2. **Update Dependencies**
   ```bash
   pip install -r requirements.txt
   npm install
   ```

3. **Run Database Migrations** (if applicable)
   ```bash
   python manage.py migrate
   ```

## Security Notes

- Keep your dependencies up to date
- Never commit sensitive data
- Use environment variables for secrets
- Regularly update your Python and Node.js versions

## License

This project is licensed under the MIT License - see the LICENSE file for details.