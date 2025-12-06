# Crysta Agent Template

CrystaCode uses this repository to store and manage templates for AI agents that can be deployed using the CrystaCode platform. Each template defines the structure, behavior, and characteristics of a specific type of AI agent.

The **Agent Studio** uses these templates to render the editor UI, and instruct editor's AI to ask questions based on the template's prompt variables to help users configure their AI agents effectively.

# Template Structure
All predefined templates are stored in the `templates/` directory. Each template has its own subdirectory containing the following key files:
- `template.json`: The main configuration file defining the template's metadata, prompt variables, and other settings.
- `template.md`: A markdown file that outlines the prompt structure and instructions for the AI agent

Check the full specification of the template structure in the [Template Specification](docs/template-spec.md) document.

# Predefined Templates
Here are some of the predefined templates available in this repository:
- **Lead Generation Agent**: An AI agent designed to assist businesses in generating high-quality leads by engaging with potential customers and collecting their contact information. [Template Details](templates/lead-generation/template.json)
- **Real Estate Agent Assist**: An AI agent designed to assist real estate agents in managing client inquiries and generating leads. [Template Details](templates/real-estate-agent-assist/template.json)