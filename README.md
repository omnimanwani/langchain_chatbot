# LangChain Chatbot Project

## Overview
This project implements a chatbot using LangChain, an open-source framework for creating conversational agents. The chatbot is designed to provide compassionate medical professional responses to user queries, leveraging various tools, including a custom search tool for Physiopedia. The conversation history is maintained, and the chatbot is capable of answering questions in a step-by-step manner.

## Setup
To run this project, ensure you have the required dependencies installed. You can install them using the following commands:

```bash
!pip -q install cohere openai
!pip -q install --upgrade pip
!pip -q install langchain duckduckgo-search
!pip -q install tiktoken
!pip -q install --upgrade pip
```

Make sure to set your OpenAI API key by assigning it to the `OPENAI_API_KEY` environment variable.

```python
import os

os.environ["OPENAI_API_KEY"] = "your_openai_api_key"
```

## Usage
1. Clone the repository.
2. Install the required dependencies.
3. Set your OpenAI API key.
4. Run the script.

```python
python your_script_name.py
```

## Customization
- **Tools**: You can customize the tools available to the chatbot by modifying the `tools` list in the script. Each tool has a name, function, and description.

```python
Tool(
    name="Your Tool Name",
    func=your_tool_function,
    description="Describe your tool"
)
```

- **Template**: Customize the chatbot's response template by modifying the `template_with_history` variable in the script. This template includes placeholders for tools, thoughts, actions, and final answers.

## Conversational Flow
1. The chatbot begins by introducing itself and providing information about available tools.
2. The user asks a question.
3. The chatbot processes the question, performs actions using available tools, and records thoughts and observations.
4. The chatbot iteratively provides thoughts, actions, and observations until it reaches a final answer.
5. The chatbot delivers the final answer in a compassionate and professional manner.
6. The conversation history is updated with each interaction.

## Notes
- The chatbot is designed to run continuously until the user types 'exit.'

Feel free to explore, modify, and enhance the chatbot for different use cases or industries. If you encounter any issues or have suggestions, please contribute to the project.

Happy chatting!
