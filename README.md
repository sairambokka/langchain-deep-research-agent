# LangChain Deep Research Agent

A sophisticated AI-powered research agent built with LangGraph that conducts comprehensive research and generates detailed reports on any topic. The agent leverages multiple specialized sub-agents to perform in-depth research, critique findings, and produce high-quality research documents.

## Overview

This project implements a multi-agent research system that can:
- Conduct thorough internet research using the Tavily search API
- Break down complex research topics into manageable sub-questions
- Generate comprehensive, well-structured research reports
- Self-critique and iteratively improve research quality
- Support multiple languages for both input and output

## Architecture

The system consists of three main components:

### 1. Main Research Agent
The primary orchestrator that:
- Manages the overall research workflow
- Coordinates between specialized sub-agents
- Writes and refines the final research report
- Maintains research context and question tracking

### 2. Research Sub-Agent
A dedicated researcher that:
- Conducts focused research on specific topics
- Uses internet search to gather comprehensive information
- Provides detailed answers to research questions
- Handles one topic at a time for optimal depth

### 3. Critique Sub-Agent
An editor and quality assurance agent that:
- Reviews the final research report for completeness
- Checks structure, clarity, and comprehensiveness
- Identifies areas for improvement
- Ensures reports meet academic and professional standards

## Key Features

### Intelligent Research Workflow
- **Topic Decomposition**: Automatically breaks down complex questions into focused research areas
- **Parallel Processing**: Conducts multiple research streams simultaneously for efficiency
- **Iterative Improvement**: Uses critique feedback to enhance report quality

### Comprehensive Report Generation
- **Structured Output**: Generates well-organized reports with proper headings and sections
- **Source Citations**: Includes numbered citations with source references
- **Multiple Formats**: Supports various report structures (comparisons, lists, overviews, summaries)
- **Professional Quality**: Produces publication-ready research documents

### Advanced Search Capabilities
- **Tavily Integration**: Leverages advanced web search APIs for current information
- **Configurable Results**: Adjustable search depth and content inclusion
- **Multi-language Support**: Researches and reports in the user's preferred language

## Technical Implementation

### Dependencies
- **LangChain**: Core AI framework for agent orchestration
- **LangGraph**: Graph-based agent workflow management
- **Tavily**: Professional web search API for research
- **Anthropic**: Language model integration (default)
- **DeepAgents**: Custom agent framework

### Environment Setup
The project uses a Python virtual environment (`deepresearch/`) with Python 3.13.5 and requires:
- `TAVILY_API_KEY`: API key for Tavily search service
- `ANTHROPIC_API_KEY`: Anthropic API credentials (default model provider)

### Configuration
- **LangGraph Config**: Defined in `langgraph.json` with research graph endpoint
- **Recursion Limit**: Set to 1000 for deep research capabilities
- **Environment Variables**: Managed through `.env` file

## Usage Workflow

1. **Question Input**: User provides a research question or topic
2. **Question Storage**: System saves the original question to `question.txt`
3. **Research Planning**: Main agent analyzes and breaks down the research scope
4. **Information Gathering**: Research sub-agents conduct focused searches
5. **Report Writing**: Main agent compiles findings into `final_report.md`
6. **Quality Review**: Critique agent reviews and suggests improvements
7. **Refinement**: Iterative research and editing until quality standards are met

## Report Quality Standards

The system ensures reports meet professional standards by checking:
- **Structure**: Proper headings, sections, and logical flow
- **Comprehensiveness**: Complete coverage of the research topic
- **Depth**: Detailed analysis with insights and trends
- **Clarity**: Clear, accessible language and presentation
- **Citations**: Proper source attribution and reference formatting
- **Relevance**: Direct answers to the original research question

## File Structure

```
langchain-deep-research-agent/
├── research_agent.py          # Main agent implementation
├── langgraph.json            # LangGraph configuration
├── deepresearch/             # Python virtual environment
├── .env                      # Environment variables
├── question.txt              # Current research question (generated)
├── final_report.md           # Generated research report (output)
└── README.md                 # This documentation
```

## Getting Started

1. **Environment Setup**:
   - Activate the virtual environment: `source deepresearch/bin/activate`
   - Set required API keys in `.env` file

2. **API Keys Required**:
   - Tavily API key for web search functionality
   - Anthropic API key for language model access

3. **Run the Agent**:
   - Execute the research agent through LangGraph
   - Provide your research question when prompted

4. **Review Results**:
   - Check `final_report.md` for the comprehensive research report
   - Review `question.txt` to confirm the research scope

## Advanced Features

### Multi-Agent Coordination
- Parallel research execution for complex topics
- Intelligent task distribution between specialized agents
- Conflict resolution for file operations

### Quality Assurance
- Automated report critique and improvement suggestions
- Iterative refinement process until quality standards are met
- Comprehensive fact-checking and source verification

### Customization Options
- Adjustable search parameters and result limits
- Configurable report structures and formats
- Language-specific output generation

This research agent represents a sophisticated approach to automated research, combining the power of modern AI with structured workflows to produce high-quality, comprehensive research reports on virtually any topic.