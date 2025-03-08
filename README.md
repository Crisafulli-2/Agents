## Job Application Agent
An intelligent, automated system for job searching, application submission, and networking across multiple job boards with ATS (Applicant Tracking System) compatibility.

### Features

- ATS-Compatible Resume Handling: Ensure your resume passes through ATS systems with optimization and compatibility checks
- Smart Job-Resume Matching: Analyzes job descriptions and matches them with your resume(s) for optimal application strategy
- Automated Application Submission: Completes application forms and answers screening questions intelligently across different platforms
- Networking Assistance: Identifies mutual connections and hiring managers to enhance application success
- Customizable Parameters: Configure the agent to focus on specific industries, locations, or job types

## Component Explanation
- `src/ats/` - Code for ensuring resumes are ATS-compatible and can pass through screening systems
- `src/matching/` - Contains the logic for comparing job descriptions with resumes and determining compatibility scores
- `src/application/` - Handles form filling and question answering across different job boards through dedicated adapters
- `src/networking/` - Finds mutual connections and identifies hiring managers
- `src/agent/` - The core agent that coordinates tasks, handles parameters, and manages the application workflow
- `data/` - Stores resumes, response templates, and credentials (gitignored for security)
- `config/` - Contains configuration files for different job boards and default parameters

## Getting Started
### Prerequisites
