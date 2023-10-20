---
title: ImportFormatMode Enum
linktitle: ImportFormatMode
articleTitle: ImportFormatMode
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.ImportFormatMode 枚举. 指定从另一个文档导入内容时如何合并格式 在 C#.
type: docs
weight: 3230
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
| KeepSourceFormatting | `1` | 将所有必需的样式复制到目标文档，如果需要，生成唯一的样式名称。 |
| KeepDifferentStyles | `2` | 仅复制与源文档中的样式不同的样式。 |

## 评论

当您将节点从一个文档复制到另一个文档时，此选项指定当两个文档具有名称相同但格式不同的样式时如何解析formatting 。

格式化解决如下：

1. 内置样式使用与区域设置无关的样式标识符进行匹配。 用户定义的样式使用区分大小写的样式名称进行匹配。
2. 如果在目标文档中找不到匹配的样式，则 style （及其引用的所有样式）将被复制到目标 document 中，并且更新导入的节点以引用新样式。
3. 如果目标文档中已存在匹配的样式，则发生的情况 取决于`导入格式模式`参数传递给 [`文档.导入节点`](../documentbase/importnode/) 如下所述。

当使用UseDestinationStyles选项，如果目标文档中已存在 匹配的样式，则不会复制该样式，并且更新导入的节点 以引用现有样式。

使用的缺点UseDestinationStyles问题是，与源文档相比，导入的文本在目标文档中可能 看起来有所不同。 例如，源文档中的“标题 1”样式使用 Arial 16pt 字体，而 目标文档中的“标题 1”样式使用 Times New Roman 14pt 字体。 当导入没有其他直接格式的“标题 1”样式的文本时，它将 在目标文档中显示为 Times New Roman 14pt 字体。

KeepSourceFormatting选项允许确保导入的内容在目标文档中看起来与在源文档中看起来相同 。 如果目标文档中已存在匹配的样式，则源样式格式将扩展 到直接节点属性中，并且样式为更改为 Normal。 如果目标文档中不存在该样式，则将源样式导入 到目标文档中并应用到导入的节点。 请注意，即使源样式存在，也并不总是能够保留源样式目标文档中不存在。 在这种情况下，此类样式的格式将扩展为直接节点属性，有利于保留原始节点格式。

使用的缺点KeepSourceFormatting问题是，如果您执行多次导入， 可能会在目标文档中得到多种样式，这可能会导致在 Microsoft Word 中使用 一致的样式格式对该文档变得困难。

使用KeepDifferentStyles选项允许重用目标样式 （如果它们提供的格式与源文档中的样式相同）。 如果目标文档中的样式与源文档中的样式不同，则将其导入。

## 例子

演示如何将一个文档插入到另一个文档中。

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
