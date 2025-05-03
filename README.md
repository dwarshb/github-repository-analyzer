# GitHub Repository Analyzer

A web application that analyzes GitHub repositories and generates comprehensive documentation about their features, functions, and structure.

## Features

- **API-Based Analysis**: Uses GitHub's API to analyze repositories without local cloning
- **Repository Overview**: Provides basic information about the repository (stars, forks, etc.)
- **Code Analysis**: Identifies key functions and classes in the codebase
- **Technology Detection**: Automatically detects programming languages and frameworks
- **Structure Visualization**: Displays the repository's directory structure
- **Documentation Export**: Generates downloadable Markdown documentation

## Screenshots

![Main Page](screenshots/main_page.png)
![Results Page](screenshots/results_page.png)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/github-repo-analyzer.git
   cd github-repo-analyzer
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python github_analyzer_web.py
   ```

4. Open your browser and navigate to `http://localhost:5000`

## Usage

1. Enter a GitHub repository URL in the form (e.g., `https://github.com/username/repository`)
2. Optionally provide a GitHub API token for higher rate limits and access to private repositories
3. Click "Analyze Repository" and wait for the analysis to complete
4. View the generated documentation and download it if needed

## API Usage

You can also use the analyzer programmatically through the API:

```bash
curl -X POST http://localhost:5000/api/analyze \
  -H "Content-Type: application/json" \
  -d '{"repo_url": "https://github.com/username/repository", "github_token": "your_token"}'
```

## Project Structure

```
├── github_analyzer_api.py    # GitHub API interaction module
├── github_analyzer_web.py    # Flask web application
├── requirements.txt          # Python dependencies
├── templates/                # HTML templates
│   ├── index.html            # Main page template
│   └── results.html          # Results page template
└── README.md                 # This file
```

## How It Works

1. **API Integration**: The application uses GitHub's REST API to fetch repository data
2. **Code Analysis**: It analyzes code files to extract functions, classes, and other elements
3. **Feature Detection**: It identifies technologies based on file patterns and code signatures
4. **Documentation Generation**: It creates a structured Markdown document with all findings


## Future Enhancements

- Add code quality metrics
- Generate dependency graphs
- Implement deeper code analysis for specific languages
- Add user authentication for saving analysis results
- Support for GitLab and Bitbucket repositories

## License

MIT License
