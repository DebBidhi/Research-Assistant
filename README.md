# Research Crew AI Project

A sophisticated AI-powered research automation system built with [CrewAI](https://crewai.com/) that orchestrates multiple AI agents to conduct research, summarize findings, and perform fact-checking.

## Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Example Research](#example-research)
- [Contributing](#contributing)
- [License](#license)

## Overview

The Research Crew AI Project leverages the [CrewAI framework](https://crewai.com/) to create a seamless research automation pipeline. It employs three specialized AI agents that collaborate to deliver accurate and concise research outputs:

- **Research Agent**: Gathers primary data using the [Serper API](https://serper.dev/).
- **Summarization Agent**: Condenses and organizes research findings into structured reports.
- **Fact Checker Agent**: Verifies the accuracy of the collected and summarized information.

This modular system is designed for flexibility, enabling users to customize agent behaviors and tasks for various research needs.

example.png

eample_citation.png

## Project Structure

```
.
├── research_crew.py     # Main implementation of the Research Crew
├── config/             
│   ├── agents.yaml     # Configuration for AI agents
│   └── tasks.yaml      # Task definitions and parameters
└── .env                # Environment variables and API keys
```

## Features

- **Modular Agent Architecture**: Three distinct AI agents working collaboratively.
- **Sequential Processing**: Tasks are executed in a logical sequence for optimal results.
- **API Integration**: Leverages the Serper API for powerful web search capabilities.
- **Configurable**: Customize agent behaviors and tasks via YAML configuration files.

## Prerequisites

Before setting up the project, ensure you have the following:

- **Python 3.x**: A compatible Python version installed.
- **CrewAI Library**: The core framework for agent-based workflows.
- **Serper API Key**: Required for web search functionality. Obtain one from [Serper](https://serper.dev/).

## Installation

Follow these steps to set up the project on your local machine:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo/research-crew-ai.git
   cd research-crew-ai
   ```

2. **Install Dependencies**:
   ```bash
   pip install crewai crewai-tools
   ```

3. **Configure Environment Variables**:
   - Create a `.env` file in the project root:
     ```bash
     touch .env
     ```
   - Add your Serper API key and LLM configuration (e.g., OpenAI API key):
     ```
     SERPER_API_KEY=your_serper_api_key_here
     OPENAI_API_KEY=your_openai_api_key_here
     ```
   - **Note**: CrewAI requires a language model (LLM) to operate. Configure your preferred LLM provider in the `.env` file. Refer to the [CrewAI documentation](https://crewai.com/docs) for supported LLMs and setup instructions.

## Usage

Run the research pipeline with a simple Python script:

```python
from research_crew import ResearchCrew

# Initialize the research crew
crew = ResearchCrew()

# Execute the research pipeline
results = crew.crew()
```

This will trigger the agents to perform their tasks and return the results.

## Configuration

Customize the system using the following configuration files in the `config/` directory:

- **`agents.yaml`**: Defines the properties, roles, and capabilities of each AI agent.
- **`tasks.yaml`**: Specifies the parameters and requirements for research tasks.

These YAML files allow you to tailor the system to your specific research goals without altering the core codebase.

## Example Research

Here's a simplified overview of how the agents collaborate:

1. **Research Agent**: Queries the Serper API for data on "The Future of LiDAR Technology in Autonomous Vehicles and Robotics."
2. **Summarization Agent**: Produces a concise report from the gathered data.
3. **Fact Checker Agent**: Validates the report's accuracy.

For a detailed example, including agent logs, see [Lider_research](./Lider_research.ipynb) 

