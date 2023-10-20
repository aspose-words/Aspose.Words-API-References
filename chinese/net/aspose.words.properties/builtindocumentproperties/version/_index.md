---
title: BuiltInDocumentProperties.Version
linktitle: Version
articleTitle: Version
second_title: 用于 .NET 的 Aspose.Words
description: BuiltInDocumentProperties Version 财产. 表示创建文档的应用程序的版本号 在 C#.
type: docs
weight: 320
url: /zh/net/aspose.words.properties/builtindocumentproperties/version/
---
## BuiltInDocumentProperties.Version property

表示创建文档的应用程序的版本号。

```csharp
public int Version { get; set; }
```

## 评论

当 Microsoft Word 创建文档时，高 16 位代表 主版本，低 16 位代表内部版本号。

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
