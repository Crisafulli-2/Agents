# Job Application Agent

An intelligent, automated system for job searching, application submission, and networking across multiple job boards with ATS (Applicant Tracking System) compatibility.

## Features

- **ATS-Compatible Resume Handling**: Ensure your resume passes through ATS systems with optimization and compatibility checks
- **Smart Job-Resume Matching**: Analyzes job descriptions and matches them with your resume(s) for optimal application strategy
- **Automated Application Submission**: Completes application forms and answers screening questions intelligently across different platforms
- **Networking Assistance**: Identifies mutual connections and hiring managers to enhance application success
- **Customizable Parameters**: Configure the agent to focus on specific industries, locations, or job types

## Getting Started

### Prerequisites

- Python 3.8+
- Job board account credentials (LinkedIn, Indeed, Glassdoor, etc.)
- One or more resumes in PDF or DOCX format

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/job-application-agent.git
cd job-application-agent

# Set up a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Install the package
pip install -e .
```

### Configuration

Copy `config/example_credentials.json` to `data/credentials/credentials.json` and add your job board login credentials. Place your resume(s) in the `data/resumes/` directory. Adjust parameters in `config/default_params.json` to match your job search criteria.

## Usage

### Basic Job Search and Application

```python
from job_agent import JobApplicationAgent

# Initialize the agent
agent = JobApplicationAgent(
    resume_path="data/resumes/my_resume.pdf",
    job_boards=["linkedin", "indeed"],
    job_titles=["Software Engineer", "Developer"],
    locations=["San Francisco", "Remote"]
)

# Start the automated job search and application process
agent.run()
```

### Customizing Question Responses

Create a template file in `data/responses/custom_answers.json`:

```json
{
  "salary_expectations": "My salary expectations are in the range of $X-$Y, depending on the total compensation package.",
  "notice_period": "I can start within two weeks of receiving an offer."
}
```

Then use it in your agent:

```python
agent = JobApplicationAgent(
    resume_path="data/resumes/my_resume.pdf",
    custom_responses="data/responses/custom_answers.json"
)
```

## Component Details

### ATS Scanner

The ATS Scanner ensures your resume is properly parsed by applicant tracking systems by:

- Checking for compatible formatting
- Verifying keyword presence
- Suggesting improvements for better matching

### Job-Resume Matching

The matching system:

- Extracts key requirements from job descriptions
- Analyzes your resume for relevant skills and experiences
- Provides a compatibility score
- Suggests customizations to improve matching

### Application Automation

Handles the tedious part of job applications:

- Fills out common fields (name, contact, education, experience)
- Intelligently answers screening questions based on the job context
- Adapts to different job board interfaces

### Networking Module

Enhances your application by:

- Finding mutual connections with the company or hiring team
- Identifying the hiring manager when possible
- Suggesting connection strategies

## Contributing

Contributions are welcome! Please see our Contributing Guidelines for more details.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

This tool is designed to assist with job applications, not to submit misleading information. Always ensure the information submitted is accurate and truthful. Some job boards may have terms of service that restrict automation - use responsibly and in accordance with each platform's policies.