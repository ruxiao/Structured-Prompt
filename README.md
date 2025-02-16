# AI Agent Runner

This project is designed to build an AI agent that, given a task description (e.g. "TTS singing imitation", "music track separation", "text-to-image", etc.), automatically searches for and clones relevant open source projects on GitHub, then attempts to run these projects locally (or on the cloud if high GPU requirements exist).

## Features

- **Task Parsing**: Analyzes the input task description to determine the target domain (e.g. TTS).
- **Project Search**: Searches GitHub for relevant projects based on the task description (this example uses simple condition checks; a real implementation could integrate the GitHub API).
- **Project Cloning and Installation**: Automatically clones the target project and installs required dependencies (for example, by reading a `requirements.txt` file).
- **Project Execution**: Attempts to run the project's main entry point.
- **Reinforcement Learning (RL) Optimization**: If the project fails to run, the system can utilize an RL mechanism to adjust the execution pipeline. This demo illustrates the concept and can be expanded with a full RL algorithm.

## Installation and Usage

1. **Clone this repository**:  
   ```bash
   git clone https://github.com/ruxiao/Structured-Prompt.git
2. Create and activate a Python virtual environment:
   ```bash
      python -m venv venv
      source venv/bin/activate #For Linux/Mac
      venv\Scripts\activate #For WIndows

3. Install dependencies
   ```bash
      pip install -r requirements.txt

4.Run the agent (for example, for the task "TTS singing imitation"):
   ```bash
      python main.py --task "TTS singing imitation"


