
# Introduction to Template Specification

A template is basically a JSON configuration file that defines the structure, behavior, and characteristics of an AI agent. It includes metadata about the template, prompt variables that users can configure, and instructions for how the AI should behave.

This is a very simple example of a template configuration file:

```json
{
  "code": "example-agent",
  "title": "Example Agent",
  "description": "An example AI agent template.",
  "version": "1.0",
  "template": "Answer the user's questions about their my business. My buisness is described as follows: `${business-description}`",
  "editor-llm-description": "[IMPORT]",
  "prompt-variables": [
    {
      "code": "business-description",
      "title": "Business Description",
      "display-description": "A description of the business.",
      "editor-llm-description": "Ask about the client's business specifics like location, their products, and services.",
      "ui-type": "textarea",
      "ui-group": "basic",
      "order": 1,
      "is-visible": true,
      "default-value": null,
      "placeholder": "e.g. A local bakery specializing in artisan bread and pastries."
    }
  ],
  "ui-groups": [
    {
      "code": "basic",
      "title": "Basic Information",
      "order": 1
    }
  ]
}
```

In this example, the template defines an AI agent called "Example Agent" that answers questions about a business. It includes one prompt variable, "business-description", which users can fill in to provide context about their business. The template also specifies how the AI should use this information in its responses.

The template structure typically includes the following key components:
- **Metadata**: Information about the template such as its code, title, description, and version.
- **Template**: The main prompt structure that guides the AI's behavior.
- **Editor LLM Description**: Instructions for the editor's AI to help users configure the agent effectively.
- **Prompt Variables**: A list of variables that users can configure to customize the AI agent's behavior.
- **UI Groups**: Definitions for organizing the prompt variables in the user interface.

# Importing Content
Templates can also import content from other markdown files to keep the configuration organized and modular. This is done using the `[IMPORT]` directive in the `template` or `editor-llm-description` fields. The imported files typically contain detailed descriptions for prompt variables or the main prompt structure.

For example, a template might import its main prompt structure from a `template.md` file and detailed descriptions for its prompt variables from an `editor-llm-description.md` file and additional files in a `prompt-variables/` directory.
For prompt variables, the imported files are usually named according to the variable they describe, such as `business-description.editor-llm-description.md`.

# Example Template Files
Here are some examples of template files that illustrate the structure and components discussed above:  
- `templates/lead-generation/template.json`: Configuration for a lead generation AI agent.
- `templates/real-estate-agent-assist/template.json`: Configuration for a real estate agent assist AI agent.
- 
 


