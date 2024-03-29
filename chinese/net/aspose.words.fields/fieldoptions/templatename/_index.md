---
title: FieldOptions.TemplateName
linktitle: TemplateName
articleTitle: TemplateName
second_title: 用于 .NET 的 Aspose.Words
description: FieldOptions TemplateName 财产. 获取或设置文档使用的模板的文件名 在 C#.
type: docs
weight: 190
url: /zh/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

获取或设置文档使用的模板的文件名。

```csharp
public string TemplateName { get; set; }
```

## 评论

该属性由[`FieldTemplate`](../../fieldtemplate/)字段如果[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/)财产是空的。

如果该属性为空，则默认模板文件名`正常.dotm`用来。

## 例子

演示如何使用 TEMPLATE 字段来显示文档模板的本地文件系统位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们可以通过字段设置模板名称。当“doc.AttachedTemplate”为空时使用此属性。
// 如果此属性为空，则使用默认模板文件名“Normal.dotm”。
doc.FieldOptions.TemplateName = string.Empty;

FieldTemplate field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
Assert.AreEqual(" TEMPLATE ", field.GetFieldCode());

builder.Writeln();
field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
field.IncludeFullPath = true;

Assert.AreEqual(" TEMPLATE  \\p", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TEMPLATE.docx");
```

### 也可以看看

* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
