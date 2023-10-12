---
title: FieldOptions.FieldIndexFormat
second_title: Aspose.Words for .NET API 参考
description: FieldOptions 财产. 获取或设置FieldIndexFormat代表 的格式FieldIndex文档中的字段.
type: docs
weight: 90
url: /zh/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

获取或设置`FieldIndexFormat`代表 的格式[`FieldIndex`](../../fieldindex/)文档中的字段.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

### 例子

演示如何设置 FieldIndex 字段的格式。

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
* 命名空间 [Aspose.Words.Fields](../../fieldoptions/)
* 部件 [Aspose.Words](../../../)


