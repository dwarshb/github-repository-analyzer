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

![Screenshot 2025-05-03 at 10 22 32 PM](https://github.com/user-attachments/assets/77da03f0-3b0a-4ec4-af1e-6f17473a7dd7)
### Result Analysis
| Overview | Structure | Code Analysis |
|---|---|---|
|![Screenshot 2025-05-04 at 2 06 29 AM](https://github.com/user-attachments/assets/500ffcc8-382c-4961-b960-8ef8f7a673f9) | ![Screenshot 2025-05-04 at 2 06 39 AM](https://github.com/user-attachments/assets/80584bfd-dfee-4225-9f20-97c39b6bcdc0)|![Screenshot 2025-05-04 at 2 06 58 AM](https://github.com/user-attachments/assets/21f7beb0-14a1-4b19-8cdf-e87b5888d9f7)|


## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/dwarshb/github-repository-analyzer.git
   cd github-repository-analyzer
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
