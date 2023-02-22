---
title: BuiltInDocumentProperties.Template
second_title: Aspose.Words for .NET API 参考
description: BuiltInDocumentProperties 财产. 获取或设置文档模板的信息名称
type: docs
weight: 270
url: /zh/net/aspose.words.properties/builtindocumentproperties/template/
---
## BuiltInDocumentProperties.Template property

获取或设置文档模板的信息名称。

```csharp
public string Template { get; set; }
```

### 评论

在 Microsoft Word 中，此属性仅供参考， 通常只包含模板的文件名而不包含路径。

空字符串表示文档附加到 Normal 模板。

要获取或设置附加模板的实际名称，请使用 [`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/)财产。

### 例子

显示如何使用“来源”类别中的文档属性。

```csharp
// 打开我们使用 Microsoft Word 创建和编辑的文档。
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// 以下内置属性包含有关创建和编辑此文档的信息。
// 我们可以在 Windows 资源管理器中右键单击该文档并找到
// 这些属性通过“属性”-> “详细信息”-> “起源”类别。
// PRINTDATE 和 EDITTIME 等字段可以在文档正文中显示这些值。
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// 我们也可以改变内置属性的值。
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// 当我们保存文档时，Microsoft Word 会自动更新以下属性。
// 要将这些属性与 Aspose.Words 一起使用，我们需要手动为它们设置值。
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// 我们可以在 Windows 资源管理器中右键单击该文档并找到 these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### 也可以看看

* class [BuiltInDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../builtindocumentproperties/)
* 部件 [Aspose.Words](../../../)


