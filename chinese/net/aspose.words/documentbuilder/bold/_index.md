---
title: DocumentBuilder.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words for .NET
description: 探索 DocumentBuilder 的粗体属性。轻松将字体设置为粗体，增强文本在文档中的可见性和视觉冲击力。立即提升您的设计水平！
type: docs
weight: 20
url: /zh/net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

如果字体格式为粗体，则为真。

```csharp
public bool Bold { get; set; }
```

## 例子

展示如何使用文档生成器而不是邮件合并来填充 MERGEFIELDs 数据。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一些 MERGEFIELDS，它们在邮件合并期间接受来自数据源中同名列的数据，
//然后手动填充它们。
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
