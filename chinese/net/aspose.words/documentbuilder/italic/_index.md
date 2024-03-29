---
title: DocumentBuilder.Italic
linktitle: Italic
articleTitle: Italic
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder Italic 财产. 如果字体格式为斜体则为 True 在 C#.
type: docs
weight: 140
url: /zh/net/aspose.words/documentbuilder/italic/
---
## DocumentBuilder.Italic property

如果字体格式为斜体，则为 True。

```csharp
public bool Italic { get; set; }
```

## 例子

演示如何使用文档生成器而不是邮件合并来填充数据MERGEFIELD。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一些 MERGEFIELDS，它们在邮件合并期间接受数据源中同名列的数据，
// 然后手动填充它们。
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
