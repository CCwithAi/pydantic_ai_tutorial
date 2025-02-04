# Introduction

This repository contains examples and explanations of how to use [PydanticAI](https://ai.pydantic.dev/) - a Python Agent Framework designed to make it easier to build production-grade applications with Generative AI.

Intro to PydanticAI

PydanticAI is a Python agent framework designed to make it less painful to build production grade applications with Generative AI.

FastAPI revolutionized web development by offering an innovative and ergonomic design, built on the foundation of Pydantic.

##Pydantic AI Core Concepts

1. [Agents](https://ai.pydantic.dev/agents/): The primary interface for interacting with LLMs, allowing you to define system prompts and manage interactions.
2. [Dependencies](https://ai.pydantic.dev/dependencies/): A type-safe system for injecting runtime context and accessing external services, making testing and integration easier.
3. [Results](https://ai.pydantic.dev/results/): Agents can return plain text, structured data, or streamed responses, all validated by Pydantic models.
4. [Messages and Chat History](https://ai.pydantic.dev/message-history/): Provides access to complete message history and tools for analyzing agent behavior and continuing conversations.
5. [Testing and Evals](https://ai.pydantic.dev/testing-evals/): Supports unit tests and evaluations to assess model performance and ensure application reliability.
6. [Debugging and Monitoring](https://ai.pydantic.dev/logfire/): Integrates with Pydantic Logfire for real-time debugging, performance monitoring, and querying of agent runs.

##Getting Started

To begin using PydanticAI, follow these steps:

1- *Python**: Ensure you have Python installed on your system. PydanticAI requires Python 3.9 or later.

2- *Install Requirements**: Navigate to the root directory of the repository and install the necessary dependencies by running:

    ```bash
    pip install -r requirements.txt
    ```

3-  Environment Variables: USE `.env.example` file to a new file named `.env`. Open the `.env` file and add your OpenAI API key:

    ```bash
    OPENAI_API_KEY=your_openai_api_key_here
    ```

    Make sure to replace `your_openai_api_key_here` with your actual OpenAI API key.

4- RUN THE SCRIPT: To see how PydanticAI works, execute the `introduction.py` script:


For more detailed examples and documentation, refer to the [PydanticAI documentation](https://ai.pydantic.dev/).


PROBLEMS: I couldn't find a way to adjust model temperature.

Also a problem with message history when using tools. I got the following error:

  ```
  BadRequestError: Error code: 400 - {'error': {'message': "An assistant message with 'tool_calls' must be followed by tool messages responding to each 'tool_call_id'. The following tool_call_ids did not have response messages: call_KMMn5Bo6wPN3aZosdstleZO2", 'type': 'invalid_request_error', 'param': 'messages.[6].role', 'code': None}}
  ```