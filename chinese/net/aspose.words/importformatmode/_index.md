---
title: ImportFormatMode Enum
linktitle: ImportFormatMode
articleTitle: ImportFormatMode
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.ImportFormatMode 如何通过无缝合并导入内容的样式来增强文档格式以获得最佳效果。
type: docs
weight: 3680
url: /zh/net/aspose.words/importformatmode/
---
## ImportFormatMode enumeration

指定从另一个文档导入内容时如何合并格式。

```csharp
public enum ImportFormatMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| UseDestinationStyles | `0` | 使用目标文档样式并复制新样式。这是默认选项。 |
| KeepSourceFormatting | `1` | 将所有需要的样式复制到目标文档，如有必要，生成唯一的样式名称。 |
| KeepDifferentStyles | `2` | 仅复制与源文档不同的样式。 |

## 评论

当您将节点从一个文档复制到另一个文档时，此选项指定当两个文档具有相同名称但不同格式的样式时如何解析 formatting 。

格式解析如下：

1. 内置样式使用与语言环境无关的样式标识符进行匹配。 用户定义的样式使用区分大小写的样式名称进行匹配。
2. 如果在目标文档中找不到匹配的样式，则 style （及其引用的所有样式）将被复制到目标 document 中，并且导入的节点将更新以引用新样式。
3. 如果目标文档中已经存在匹配的样式，则会发生什么 取决于`导入格式模式`参数传递给 [`ImportNode`](../documentbase/importnode/) 如下所述。

使用时UseDestinationStyles选项，如果目标文档中已经存在匹配的样式，则不会复制该样式，并且会更新导入的节点以引用现有样式。

使用UseDestinationStyles导入的文本在目标文档中看起来可能与源文档中的看起来不同。例如，源文档中的“标题 1”样式使用 Arial 16pt 字体，而目标文档中的“标题 1”样式使用 Times New Roman 14pt 字体。当导入没有其他直接格式的“标题 1”样式的文本时，它将在目标文档中显示为 Times New Roman 14pt 字体。

KeepSourceFormatting选项可以确保导入的内容在目标文档中看起来与在源文档中看起来相同。 如果目标文档中已经存在匹配的样式，则源样式格式将扩展为直接节点属性，并且样式将更改为正常。 如果目标文档中不存在该样式，则源样式将导入目标文档并应用于导入的节点。 请注意，即使目标文档中不存在源样式，也不总是能够保留源样式。 在这种情况下，此类样式的格式将扩展为直接节点属性，以便保留原始节点格式。

使用KeepSourceFormatting问题是，如果您执行多次导入， 则目标文档中可能会出现许多样式，而这可能会使在 Microsoft Word 中对该文档使用 一致的样式格式变得困难。

使用KeepDifferentStyles如果目标样式提供的格式与源文档中的样式相同，则选项允许重复使用目标样式 。 如果目标文档中的样式与源文档不同，则会导入。

## 例子

展示如何将一个文档插入到另一个文档中。

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
