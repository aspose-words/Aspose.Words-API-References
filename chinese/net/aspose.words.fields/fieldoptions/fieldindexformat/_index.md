---
title: FieldOptions.FieldIndexFormat
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words for .NET
description: 了解如何利用 FieldOptions 中的 FieldIndexFormat 属性自定义 FieldIndex 格式，以增强文档的清晰度和组织性。
type: docs
weight: 90
url: /zh/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

获取或设置`FieldIndexFormat`代表 的格式[`FieldIndex`](../../fieldindex/)文档中的字段。

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

## 例子

展示如何格式化 FieldIndex 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("A");
builder.InsertBreak(BreakType.LineBreak);
builder.InsertField("XE \"A\"");
builder.Write("B");

builder.InsertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

doc.FieldOptions.FieldIndexFormat = FieldIndexFormat.Fancy;
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.SetFieldIndexFormat.docx");
```

### 也可以看看

* enum [FieldIndexFormat](../../fieldindexformat/)
* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
