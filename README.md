# WorkflowAI

WorkflowAI is a Flask-based web application designed to streamline workflow management through voice processing, language detection, translation, and automated Minutes of Meeting (MoM) generation. It provides a user-friendly dashboard for task management and integrates with AI services for text analysis.

## Features

- **Voice Processing**: Process raw text input from voice recordings.
- **Language Detection**: Automatically detect the language of the input text.
- **Translation**: Translate text to English using advanced translation services.
- **MoM Generation**: Generate summaries, key points, and action items from meetings.
- **Task Dashboard**: Manage and track tasks with a responsive web interface.
- **Error Handling**: Robust error handling for reliable operation.

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/prem85642/WorkflowAI1.git
   cd WorkflowAI-main
   ```

2. Create a virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Initialize the database:
   ```
   python -c "import database; database.init_db()"
   ```

## Usage

1. Run the application:
   ```
   python app.py
   ```

2. Open your browser and navigate to `http://localhost:5000`.

3. Access the dashboard at `http://localhost:5000/dashboard`.

## API Endpoints

- `GET /`: Home page
- `GET /dashboard`: Task dashboard
- `POST /api/process_voice`: Process voice input (expects JSON with 'text', optional 'hf_token', 'source_lang_code')

## Deployment

The application is configured for deployment on platforms like Heroku or Render using Gunicorn.

- Procfile: `web: gunicorn app:app`
- Requirements: Listed in `requirements.txt`

## Testing

Run the test script:
```
python test_api.py
```

## Contributing

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -am 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Create a Pull Request.

## License

This project is licensed under the MIT License.