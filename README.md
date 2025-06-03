# 🚀 AI Dev Tasks for AI coding agents 🤖

Welcome to **AI Dev Tasks**! This repository provides a collection of `.mdc` (Markdown Command) files designed to supercharge your feature development workflow with any AI coding agent. By leveraging these structured commands with AI assistants like Claude, ChatGPT, GitHub Copilot Chat, Codeium, or any other AI coding tool, you can systematically approach building features from ideation to implementation with built-in checkpoints for verification.

Stop wrestling with monolithic AI requests and start guiding your AI collaborator step-by-step!

## ✨ The Core Idea

Building complex features with AI can sometimes feel like a black box. This workflow aims to bring structure, clarity, and control to the process by:

1.  **Defining Scope:** Clearly outlining what needs to be built with a Product Requirement Document (PRD).
2.  **Detailed Planning:** Breaking down the PRD into a granular, actionable task list.
3.  **Iterative Implementation:** Guiding the AI to tackle one task at a time, allowing you to review and approve each change.

This structured approach helps ensure the AI stays on track, makes it easier to debug issues, and gives you confidence in the generated code.

## 🔧 Compatible AI Coding Agents

This workflow can be adapted for use with various AI coding assistants:

- **Cursor** - Built-in agent chat with file references
- **Claude** (Anthropic) - Via web interface or API
- **ChatGPT** (OpenAI) - GPT-4 or later recommended
- **GitHub Copilot Chat** - In VS Code or other supported IDEs
- **Codeium** - Free AI coding assistant
- **Amazon Q Developer** - AWS's AI coding assistant
- **Tabnine** - AI code completion with chat features
- **Any other AI assistant** that can read files and generate code

## Workflow: From Idea to Implemented Feature 💡➡️💻

Here's the step-by-step process using the `.mdc` files in this repository:

### 1️⃣ Create a Product Requirement Document (PRD)

First, lay out the blueprint for your feature. A PRD clarifies what you're building, for whom, and why.

**For Cursor users:**
```
Use @create-prd.mdc
Here's the feature I want to build: [Describe your feature in detail]
Reference these files to help you: [Optional: @file1.py @file2.ts]
```

**For other AI agents:**
```
Please use the create-prd.mdc template to help me create a PRD.
Here's the feature I want to build: [Describe your feature in detail]

[Paste the contents of create-prd.mdc here if the AI can't access files directly]

Reference these files for context: [Paste relevant code snippets]
```

*(Pro Tip: For complex PRDs, using the most capable model available (e.g., GPT-4, Claude Opus) is recommended for comprehensive generation.)*

### 2️⃣ Generate Your Task List from the PRD

With your PRD drafted (e.g., `MyFeature-PRD.md`), the next step is to generate a detailed, step-by-step implementation plan.

**For Cursor users:**
```
Now take @MyFeature-PRD.md and create tasks using @generate-tasks-from-prd.mdc
```

**For other AI agents:**
```
Please create a detailed task list from this PRD using the generate-tasks-from-prd.mdc template:

[Paste your PRD content here]

[Paste the contents of generate-tasks-from-prd.mdc here if needed]
```

### 3️⃣ Examine Your Task List

You'll now have a well-structured task list, often with tasks and sub-tasks, ready for the AI to start working on. This provides a clear roadmap for implementation.

### 4️⃣ Instruct the AI to Work Through Tasks (and Mark Completion)

To ensure methodical progress and allow for verification, we'll use `process-task-list.mdc`. This command instructs the AI to focus on one task at a time and wait for your go-ahead before moving to the next.

**For Cursor users:**
```
Please start on task 1.1 and use @process-task-list.mdc
```

**For other AI agents:**
```
Let's work through this task list systematically. Please start with task 1.1.

Here are the instructions from process-task-list.mdc:
[Paste the contents of process-task-list.mdc]

After completing each task, please wait for my review before proceeding to the next one.
```

### 5️⃣ Review, Approve, and Progress ✅

As the AI completes each task, you review the changes:
- If the changes are good, simply reply with "yes", "approved", or "continue" to move to the next task
- If changes are needed, provide feedback to correct the current task before moving on

You'll see a satisfying list of completed items grow, providing a clear visual of your feature coming to life!

## 🗂️ Files in this Repository

*   **`create-prd.mdc`**: Template for generating a Product Requirement Document for your feature
*   **`generate-tasks-from-prd.mdc`**: Template for breaking down a PRD into a detailed implementation task list
*   **`process-task-list.mdc`**: Instructions for processing tasks one at a time with approval checkpoints

## 🎯 Adapting for Your AI Agent

### If your AI agent CAN access files directly:
- Simply reference the `.mdc` files in your prompts
- Use your agent's file reference syntax (e.g., `@filename` for Cursor, file uploads for ChatGPT)

### If your AI agent CANNOT access files directly:
1. Copy the contents of the relevant `.mdc` file
2. Paste it into your conversation when needed
3. Consider creating templates or snippets in your IDE for quick access

### Tips for different platforms:

**ChatGPT/Claude Web:**
- Upload the `.mdc` files at the start of your conversation
- Or maintain a document with all templates for easy copy-paste

**VS Code with GitHub Copilot Chat:**
- Keep the `.mdc` files open in tabs for reference
- Use the `#file` syntax to reference open files

**API-based implementations:**
- Include the `.mdc` contents in your system prompts
- Or load them programmatically as part of your context

## 🌟 Benefits

*   **Universal Compatibility:** Works with any AI coding assistant that can process text
*   **Structured Development:** Enforces a clear process from idea to code
*   **Step-by-Step Verification:** Review and approve AI-generated code at each step
*   **Manages Complexity:** Breaks down large features into digestible tasks
*   **Improved Reliability:** More dependable than single, large prompts
*   **Clear Progress Tracking:** Visual representation of completed tasks

## 🛠️ How to Use

1.  **Clone or Download:** Get these `.mdc` files into your project
2.  **Choose Your AI Agent:** Pick your preferred AI coding assistant
3.  **Follow the Workflow:** Use the 5-step process outlined above
4.  **Adapt as Needed:** Modify the templates to suit your specific needs

## 💡 Tips for Success

*   **Be Specific:** Provide clear context and instructions for better AI output
*   **Use Capable Models:** For PRD creation, use the most capable model available
*   **Iterate and Refine:** Be prepared to guide and correct the AI
*   **Save Your Context:** Keep your PRD and task list handy for reference
*   **Template Library:** Consider creating a personal library of modified templates

## 🤝 Contributing

Got ideas to improve these `.mdc` files or have new ones that fit this workflow? Contributions are welcome!
Please feel free to:
*   Open an issue to discuss changes or suggest new features
*   Submit a pull request with your enhancements
*   Share your adaptations for specific AI agents

---

Happy AI-assisted developing with your favorite AI coding agent!
