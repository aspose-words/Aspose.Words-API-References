---
title: BuiltInDocumentProperties.TotalEditingTime
linktitle: TotalEditingTime
articleTitle: TotalEditingTime
second_title: Aspose.Words for .NET
description: 探索 BuiltInDocumentProperties TotalEditingTime 属性，高效追踪文档编辑。精准的编辑时间管理，优化您的工作流程。
type: docs
weight: 340
url: /zh/net/aspose.words.properties/builtindocumentproperties/totaleditingtime/
---
## BuiltInDocumentProperties.TotalEditingTime property

获取或设置总编辑时间（分钟）。

```csharp
public int TotalEditingTime { get; set; }
```

## 例子

展示如何使用“Origin”类别中的文档属性。

```csharp
// 打开我们使用 Microsoft Word 创建和编辑的文档。
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// 以下内置属性包含有关此文档的创建和编辑的信息。
// 我们可以在 Windows 资源管理器中右键单击此文档并找到
// 这些属性通过“属性”->“详细信息”->“来源”类别。
// PRINTDATE 和 EDITTIME 等字段可以在文档正文中显示这些值。
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// 我们还可以改变内置属性的值。
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// 当我们保存文档时，Microsoft Word 会自动更新以下属性。
// 要将这些属性与 Aspose.Words 一起使用，我们需要手动为它们设置值。
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// 我们可以在 Windows 资源管理器中右键单击此文档并找到 these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### 也可以看看

* class [BuiltInDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
