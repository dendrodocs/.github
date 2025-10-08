# Welcome to DendroDocs

**DendroDocs** is an open-source project dedicated to converting Abstract Syntax Trees (ASTs) from various programming languages into meaningful, up-to-date documentation.
We currently support both .NET and Java implementations, with plans to expand to other languages.

## Features

* **Analyzers**: Tools to analyze .NET and Java projects or solutions, extracting detailed information from source code.
* **Libraries**: Core libraries that assist in generating applications to create documentation in various formats such as Markdown, AsciiDoc, PlantUML, Mermaid, and more.
* **Renderers**: Extensible rendering system to transform analyzed code into human-readable documentation.
* **Multi-language Support**: Currently supporting .NET and Java, with an architecture designed for future language expansion.

## Project Structure

Our organization consists of several key repositories:

### Tools
* **[dotnet-tool](https://github.com/dendrodocs/dotnet-tool)**: NuGet tool to analyze .NET projects/solutions, enabling schema analysis and documentation generation
* **[java-tool](https://github.com/dendrodocs/java-tool)**: Java tool to analyze JVM projects/solutions, enabling schema analysis and documentation generation

### Libraries
* **[dotnet-shared-lib](https://github.com/dendrodocs/dotnet-shared-lib)**: Shared .NET library for DendroDocs
* **[dotnet-client-lib](https://github.com/dendrodocs/dotnet-client-lib)**: .NET client library for DendroDocs

### Schema
* **[schema](https://github.com/dendrodocs/schema)**: Schema definitions for DendroDocs

### Workshops
* **[workshops](https://github.com/dendrodocs/workshops)**: Workshops to start analyzing Abstract Syntax Trees (ASTs) to generate documentation from your source code
* **[workshops-dotnet-sample-pitstop](https://github.com/dendrodocs/workshops-dotnet-sample-pitstop)**: Sample application demonstrating microservices architecture concepts for workshop scenarios

Visit our [organization page](https://github.com/dendrodocs) to explore all repositories.

## Presentation

Learn more about DendroDocs and see it in action:

*Coming soon: Watch our presentation covering real-world examples and best practices for living documentation.*

## Getting Started

### Prerequisites

* For .NET projects: .NET 6.0 SDK or newer
* For Java projects: JDK 11 or newer

### Installation

Install the appropriate analyzer for your project:

**For .NET projects:**
```shell
dotnet tool install --global DendroDocs.Analyzer
```

**For Java projects:**
```shell
# Installation instructions available in the java-tool repository
```

## Generating Documentation

Using DendroDocs to generate documentation involves a three-step process:

1. **Analyze Source Code**: Run the DendroDocs Analyzer with your solution or project file as input.
   This will generate an intermediate JSON file containing detailed information about your source code.
2. **Develop Renderers**: Create a custom "render application" to interpret the JSON file and generate various views on your source code, such as class diagrams or sequence diagrams.
3. **Output Documentation**: Export your findings in text-based formats like Markdown, AsciiDoc, PlantUML, Mermaid, etc.

Both during local development, as during your CI/CD pipeline, can follow the same flow.

### Local Development

The analysis of a solution might take some time.
Therefore, an intermediate JSON file is created to speed up the documentation generation process.
This ensures a fast feedback loop when developing your renderers.

### Develop Your Own Renderers

A renderer application can be as simple as a command line tool that takes in the generated JSON files, makes conclusions based on the type information and writes this to a plain text file format.

To get started quickly, you should make a dependency on the appropriate NuGet packages in your project:

* **DendroDocs.Shared**: Shared .NET library with core functionality
* **DendroDocs.Client**: Client library for working with DendroDocs

## Dive Deeper

For more detailed examples and advanced use cases, refer to the [DendroDocs Workshops](https://github.com/dendrodocs/workshops).

## Contributing

You are welcome to contribute! Feel free to create [issues](https://github.com/dendrodocs/.github/issues) or [pull requests](https://github.com/dendrodocs/.github/pulls).

Please read our [Contributing Guidelines](https://github.com/DendroDocs/.github/blob/main/CONTRIBUTING.md) and [Code of Conduct](https://github.com/DendroDocs/.github/blob/main/CODE_OF_CONDUCT.md) to get started.

## License

This project is licensed under the [MIT License](LICENSE).

