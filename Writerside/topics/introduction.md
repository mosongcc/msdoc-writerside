# 概述

Writerside 是一款由 JetBrains 推出的工具，主要用于协作编写文档和教程。它是一款基于 IntelliJ 平台的 IDE，既可作为 JetBrains
IDE 的插件使用，也可作为独立工具运行。

Writerside 的主要功能包括：

1. 文档即代码环境（Docs-as-code pipeline）：该工具内置了 Git UI，使用户无需过多关注布局和 CSS 设计等细节，专注于编写核心内容。
2. 支持 Markdown 和 XML 组合使用：开发者可以在 Markdown 中注入语义属性或元素以丰富内容，并将 Markdown 元素转换为 XML。
3. 文档内容检测（Doc quality automation）：内置超过 100 个测试，帮助自动检测损坏的链接、丢失的资源、不正确的属性值和非唯一 ID
   等问题。
4. 具有代码高亮显示和验证功能：实时预览（Live preview）功能使文档内容能够按照用户实际看到的方式实时显示，无需等待构建完成。

## 有哪些优点

1. 协作与整合：Writerside 的一个主要目标是在开发人员和作者之间实现有效的协作，弥合他们之间的差距。它基于开发工具（如
   Git）、拉取评审和自动检查，强制执行“文档即代码”管道流程，让整个团队能够像处理代码一样贡献、评审和跟踪变更。
   这种整合使得文档创建和编辑过程更加流畅，提高了团队协作的效率。
2. 格式支持：Writerside 支持 Markdown 和自定义的基于 XML 的标记，并允许文档作者在同一文档中组合这两种格式。例如，作者可以向
   Markdown 文档中注入语义属性。此外，Writerside 还支持动态地将 Markdown 片段转换为 XML，并将它们导入到 XML
   文档中。这种灵活性使得文档作者可以根据需要选择最适合的格式，同时保持文档的结构和语义完整性。
3. 内置检查：Writerside 内置了 100 多种检查，例如无效链接、缺失的资源、不正确的属性值等。这些内置检查可以帮助文档作者及时发现并修复问题，提高文档的质量。同时，Writerside
   还提供了预定义的设计，可以很容易进行定制，这样文档作者就不需要处理与布局和 CSS 相关的问题。
4. 实时预览：由于文档作者需要编写 XML 或 Markdown，因此 Writerside 提供了一个实时预览功能，可以立即反映每个更改并高亮显示错误。这在无法访问
   CI/CD 管道或构建时间较长的情况下特别有用，可以在不等待输出完成的情况下检查输出。
5. 语言支持：Writerside 还提供了一个基于人工智能的拼写检查器和一个由 JetBrains 构建的语法纠正器，支持超过 25
   种语言。这使得文档作者可以更方便地进行拼写和语法检查，提高文档的准确性和可读性。
6. 可扩展性：Writerside 既可以作为 JetBrains IDE 插件使用，也可以作为独立应用程序运行（Early Access Program (EAP)
   ）。这种可扩展性使得用户可以根据自己的需求选择最适合的使用方式。

## 适合人群

1. 开发人员：Writerside 是一款专门为开发者设计的工具，可以帮助他们在产品文档、API 参考、指南、教程和操作方法等方面进行更加高效的协作。
2. 文档编写人员：Writerside 提供了丰富的功能，如实时预览、内置检查等，可以帮助文档编写人员更高效地编写文档，提高文档的质量。
3. 团队成员：Writerside 支持多人协作，可以方便地共享文档和编辑内容，提高团队协作的效率。


