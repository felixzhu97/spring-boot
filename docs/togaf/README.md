# Spring Boot TOGAF Enterprise Architecture Diagrams

This directory contains PlantUML diagrams that illustrate Spring Boot's enterprise architecture following the TOGAF (The Open Group Architecture Framework) methodology.

## Overview

These diagrams provide a comprehensive view of Spring Boot's architecture across four TOGAF architecture domains:

- **Business Architecture** - Business capabilities, processes, value streams, and organizational structure
- **Application Architecture** - Application components, services, and their interactions
- **Data Architecture** - Data entities, access patterns, storage, and governance
- **Technology Architecture** - Runtime platforms, build tools, deployment technologies, and infrastructure

## Directory Structure

```
docs/togaf/
├── README.md
├── en/                          # English version
│   ├── togaf-overview.puml      # TOGAF overview diagram
│   ├── application-architecture.puml
│   ├── business-architecture.puml
│   ├── data-architecture.puml
│   └── technology-architecture.puml
└── zh/                          # Chinese version (中文版)
    ├── togaf-overview.puml
    ├── application-architecture.puml
    ├── business-architecture.puml
    ├── data-architecture.puml
    └── technology-architecture.puml
```

## Diagrams

### 1. TOGAF Overview (`togaf-overview.puml`)

Provides a high-level overview of all four architecture domains, the ADM (Architecture Development Method) phases, architecture governance, and module dependencies.

**Key Components:**
- Four architecture domains (Business, Application, Data, Technology)
- ADM phases (A through H)
- Architecture governance structure
- Spring Boot module dependency overview

### 2. Application Architecture (`application-architecture.puml`)

Illustrates the application components and their relationships within Spring Boot.

**Key Layers:**
- **Core Application Layer**: spring-boot, autoconfigure, test support
- **Web Application Layer**: WebMVC, WebFlux, WebSocket, Web Services
- **Data Access Application Layer**: JPA, JDBC, MongoDB, Cassandra, Redis, R2DBC
- **Messaging Application Layer**: Kafka, ActiveMQ, Artemis, AMQP, Pulsar
- **Security Application Layer**: Security, OAuth2 (Authorization Server, Client, Resource Server)
- **Monitoring Application Layer**: Actuator, Micrometer, Tracing

### 3. Business Architecture (`business-architecture.puml`)

Describes the business capabilities, processes, value streams, and organizational structure of Spring Boot development.

**Key Components:**
- **Business Capability Layer**: Framework development, module development, build tools, documentation, quality assurance
- **Business Process Layer**: Development process, quality process
- **Value Stream**: Quick start, out-of-the-box, production-ready, community support
- **Organization Structure**: Core team, module team, community contribution

### 4. Data Architecture (`data-architecture.puml`)

Shows the data models, access patterns, storage solutions, migration tools, and governance mechanisms.

**Key Layers:**
- **Data Entity Layer**: JPA entities, JDBC models, MongoDB documents, Cassandra models, Neo4j graphs, Redis key-value
- **Data Access Layer**: Repository interfaces, JDBC Template, Mongo Template, R2DBC Template, Redis Template
- **Data Storage Layer**: Relational databases, NoSQL databases, cache solutions
- **Data Migration Layer**: Flyway, Liquibase
- **Data Governance**: DataSource configuration, transaction management, data validation

### 5. Technology Architecture (`technology-architecture.puml`)

Depicts the technology stack, runtime platforms, build tools, deployment technologies, and infrastructure.

**Key Layers:**
- **Runtime Platform Layer**: JVM, Spring Framework
- **Web Server Layer**: Tomcat, Jetty, Netty
- **Build Tool Layer**: Gradle plugin, Maven plugin, Buildpack
- **Deployment Technology Layer**: JAR packaging, WAR packaging, Docker images
- **Development Tool Layer**: CLI, DevTools
- **Monitoring Technology Layer**: Actuator, Micrometer, OpenTelemetry
- **Infrastructure Layer**: Docker Compose, Testcontainers

## How to Use

### Prerequisites

To render these PlantUML diagrams, you need:

1. **PlantUML** - A tool to generate UML diagrams from text
   - Download from: https://plantuml.com/starting
   - Or use online editor: http://www.plantuml.com/plantuml/uml/

2. **Java** - Required to run PlantUML (if using the JAR version)

### Rendering Options

#### Option 1: Online Editor

1. Open http://www.plantuml.com/plantuml/uml/
2. Copy the content from any `.puml` file
3. Paste into the editor
4. The diagram will be rendered automatically

#### Option 2: Command Line

```bash
# Install PlantUML (example for macOS with Homebrew)
brew install plantuml

# Render a diagram
plantuml docs/togaf/en/togaf-overview.puml

# Render all diagrams in a directory
plantuml docs/togaf/en/*.puml
```

#### Option 3: IDE Plugins

Many IDEs support PlantUML with plugins:
- **IntelliJ IDEA**: PlantUML integration plugin
- **VS Code**: PlantUML extension
- **Eclipse**: PlantUML plugin

#### Option 4: Maven/Gradle Integration

You can integrate PlantUML into your build process:

**Maven:**
```xml
<plugin>
    <groupId>org.asciidoctor</groupId>
    <artifactId>asciidoctor-maven-plugin</artifactId>
    <configuration>
        <requires>
            <require>asciidoctor-diagram</require>
        </requires>
    </configuration>
</plugin>
```

**Gradle:**
```gradle
plugins {
    id 'org.asciidoctor.jvm.convert' version '3.3.2'
    id 'org.asciidoctor.jvm.diagram' version '3.3.2'
}
```

### Export Formats

PlantUML can export diagrams to various formats:

```bash
# PNG (default)
plantuml diagram.puml

# SVG
plantuml -tsvg diagram.puml

# PDF
plantuml -tpdf diagram.puml

# EPS
plantuml -teps diagram.puml
```

## Diagram Syntax

These diagrams use PlantUML's **component diagram** syntax:

- `component` - Defines a component
- `package` - Groups related components
- `-->` - Shows dependencies/relationships
- `:` - Adds labels to relationships

## Language Versions

- **English (`en/`)**: English labels and descriptions
- **Chinese (`zh/`)**: Chinese labels and descriptions (中文标签和描述)

Both versions maintain the same structure and relationships, only the language differs.

## Contributing

When updating these diagrams:

1. Maintain consistency between English and Chinese versions
2. Follow PlantUML component diagram syntax
3. Keep component relationships clear and logical
4. Update this README if adding new diagrams or major changes

## References

- [TOGAF Standard](https://www.opengroup.org/togaf)
- [PlantUML Documentation](https://plantuml.com/)
- [Spring Boot Documentation](https://spring.io/projects/spring-boot)

---

## 中文说明

### 概述

本目录包含使用 PlantUML 绘制的 Spring Boot 企业架构图，遵循 TOGAF（开放组架构框架）方法论。

### 如何使用

#### 在线编辑器

1. 打开 http://www.plantuml.com/plantuml/uml/
2. 复制任意 `.puml` 文件的内容
3. 粘贴到编辑器中
4. 图表将自动渲染

#### 命令行

```bash
# 安装 PlantUML（macOS 使用 Homebrew 示例）
brew install plantuml

# 渲染单个图表
plantuml docs/togaf/zh/togaf-overview.puml

# 渲染目录下所有图表
plantuml docs/togaf/zh/*.puml
```

### 图表说明

1. **TOGAF 总览图** - 展示四个架构域、ADM 阶段、架构治理和模块依赖
2. **应用架构图** - 展示 Spring Boot 应用组件及其关系
3. **业务架构图** - 描述业务能力、流程、价值流和组织结构
4. **数据架构图** - 展示数据模型、访问模式、存储方案和治理机制
5. **技术架构图** - 描述技术栈、运行时平台、构建工具和部署技术

### 语言版本

- **英文版 (`en/`)**：英文标签和描述
- **中文版 (`zh/`)**：中文标签和描述

两个版本保持相同的结构和关系，仅语言不同。

