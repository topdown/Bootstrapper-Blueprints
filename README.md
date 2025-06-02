# Bootstrapper-Blueprints

A community repository of project blueprints for the [Bootstrapper VS Code Extension](https://github.com/topdown/bootstrapper).

## What are Bootstrapper Blueprints?

Bootstrapper blueprints are project templates that allow you to quickly scaffold new projects with predefined file structures, code, and configurations. Each blueprint contains:

- **File Templates**: Pre-written code files with your project structure
- **Folder Structure**: Organized directory layout
- **Configuration Files**: Package.json, tsconfig.json, .gitignore, etc.
- **Documentation**: Setup instructions and usage guides

## Using These Blueprints

### Prerequisites

1. Install the [Bootstrapper VS Code Extension](https://github.com/topdown/bootstrapper)
2. Open VS Code (or Cursor, WindSurf, etc.)

### Access Community Blueprints

1. Open the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`)
2. Run `Bootstrapper: Browse Community Blueprints`
3. Browse available blueprints from this repository
4. View README documentation for detailed information
5. Download blueprints to your local collection
6. Create new projects using the downloaded blueprints

### Alternative Access

You can also access community blueprints through:
- `Bootstrapper: Manage Blueprints` → "Browse Community Blueprints"
- The blueprint management interface in VS Code

## Contributing Blueprints

We welcome contributions! Here's how to add your blueprint to the community collection:

### Repository Structure

Each blueprint should be in its own folder within the `blueprints/` directory:

```
blueprints/
├── your-blueprint-name/
│   ├── blueprint.json       # Required: Blueprint definition
│   └── README.md           # Recommended: Documentation
├── another-blueprint/
│   ├── blueprint.json
│   └── README.md
└── ...
```

### Step-by-Step Contribution

1. **Fork this repository**
2. **Create a new folder** in `blueprints/` with a descriptive name
3. **Add `blueprint.json`** with your blueprint definition
4. **Add `README.md`** with documentation (highly recommended)
5. **Test your blueprint** using the Bootstrapper extension
6. **Submit a pull request**

### Blueprint.json Format

Your `blueprint.json` should follow this structure:

```json
{
  "name": "Your Blueprint Name",
  "description": "Brief description of what this blueprint creates",
  "tags": ["tag1", "tag2", "category"],
  "files": {
    "package.json": "{\n  \"name\": \"{{PROJECT_NAME}}\",\n  \"version\": \"1.0.0\"\n}",
    "src/index.js": "console.log('Hello from {{PROJECT_NAME}}!');",
    "README.md": "# {{PROJECT_NAME}}\n\nGenerated from blueprint."
  },
  "folders": ["src", "tests", "docs"]
}
```

#### Template Variables

Use these variables in your file content for dynamic replacement:

- `{{PROJECT_NAME}}` - Project name as entered by user
- `{{PROJECT_NAME_UPPER}}` - Uppercase version
- `{{PROJECT_NAME_LOWER}}` - Lowercase version  
- `{{PROJECT_NAME_CAMEL}}` - camelCase version
- `{{PROJECT_NAME_PASCAL}}` - PascalCase version
- `{{DATE}}` - Current date (YYYY-MM-DD)
- `{{YEAR}}` - Current year

### README.md Template

Each blueprint should include a README.md with:

```markdown
# Blueprint Name

Brief description of what this blueprint creates.

## What's Included

- List of main files and folders
- Key technologies/frameworks used
- Configuration files included

## Prerequisites

- Node.js (if applicable)
- Required VS Code extensions
- Any other dependencies

## After Generation

1. Navigate to your new project folder
2. Run `npm install` (if applicable)
3. Follow setup instructions
4. Start coding!

## Project Structure

```
project-name/
├── src/
├── tests/
├── package.json
└── README.md
```

## Customization

Explain how users can modify the generated project to fit their needs.

## Related

- Link to relevant documentation
- Similar blueprints
- Useful resources
```

### Blueprint Guidelines

#### Naming Convention
- Use kebab-case for folder names: `react-typescript-app`
- Make names descriptive and specific
- Avoid generic names like "web-app" or "api"

#### File Content
- Include essential files for the project type
- Add proper file headers and comments
- Use template variables for dynamic content
- Include a .gitignore file appropriate for the technology

#### Documentation
- Always include a README.md in your blueprint folder
- Provide clear setup instructions
- Explain what the blueprint creates
- Include any prerequisites or dependencies

#### Tags
Use relevant tags to help users find your blueprint:
- **Technology**: `react`, `node`, `python`, `typescript`
- **Type**: `web-app`, `api`, `library`, `desktop-app`
- **Framework**: `express`, `fastapi`, `electron`, `vue`
- **Purpose**: `starter`, `boilerplate`, `template`

### Quality Standards

Before submitting, ensure your blueprint:

- ✅ Generates a working project
- ✅ Includes proper documentation
- ✅ Uses appropriate template variables
- ✅ Follows naming conventions
- ✅ Has relevant tags
- ✅ Includes necessary configuration files
- ✅ Works with the Bootstrapper extension

## Available Blueprints

### Web Development
- **[Static Website Starter](blueprints/Assets-Example/)** - Basic HTML, CSS, and JavaScript template for static websites

### APIs & Backend
- Coming soon...

### Desktop Applications
- Coming soon...

### Libraries & Tools
- Coming soon...

*Want to contribute? Check out our [contribution guidelines](#contributing-blueprints) above!*

## Support

- **Extension Issues**: [Bootstrapper Repository](https://github.com/topdown/bootstrapper/issues)
- **Blueprint Issues**: [Create an issue](https://github.com/topdown/Bootstrapper-Blueprints/issues) in this repository
- **Feature Requests**: Welcome via issues or discussions

## License

Blueprints in this repository are provided as-is for community use. Each blueprint may have its own license requirements - check individual blueprint README files for details.

---

**Happy coding! 🚀**