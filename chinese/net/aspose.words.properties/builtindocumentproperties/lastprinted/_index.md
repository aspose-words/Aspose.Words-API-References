---
title: BuiltInDocumentProperties.LastPrinted
linktitle: LastPrinted
articleTitle: LastPrinted
second_title: 用于 .NET 的 Aspose.Words
description: BuiltInDocumentProperties LastPrinted 财产. 获取或设置文档上次打印的日期UTC 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words.properties/builtindocumentproperties/lastprinted/
---
## BuiltInDocumentProperties.LastPrinted property

获取或设置文档上次打印的日期（UTC）。

```csharp
public DateTime LastPrinted { get; set; }
```

## 评论

对于源自 RTF 格式的文档，此属性返回上次打印操作的本地时间。

如果文档从未打印过，则此属性将返回 DateTime.MinValue。

Aspose.Words 不会更新此属性。

## 例子

展示如何使用“来源”类别中的文档属性。

```csharp
// 打开我们使用 Microsoft Word 创建和编辑的文档。
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// 以下内置属性包含有关此文档的创建和编辑的信息。
// 我们可以在Windows资源管理器中右键单击该文档并找到
// 这些属性通过“Properties”->; 「详情」-> “起源”类别。
// PRINTDATE 和 EDITTIME 等字段可以在文档正文中显示这些值。
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// 我们还可以更改内置属性的值。
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// 当我们保存文档时，Microsoft Word 会自动更新以下属性。
// 要在 Aspose.Words 中使用这些属性，我们需要手动设置它们的值。
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// 我们可以在Windows资源管理器中右键单击该文档并找到 these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### 也可以看看

* class [BuiltInDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
