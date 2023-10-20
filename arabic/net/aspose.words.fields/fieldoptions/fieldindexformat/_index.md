---
title: FieldOptions.FieldIndexFormat
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words لـ .NET
description: FieldOptions FieldIndexFormat ملكية. الحصول على أو تعيين aFieldIndexFormat الذي يمثل التنسيق لـFieldIndex الحقول في الوثيقة في C#.
type: docs
weight: 90
url: /ar/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

الحصول على أو تعيين a`FieldIndexFormat` الذي يمثل التنسيق لـ[`FieldIndex`](../../fieldindex/) الحقول في الوثيقة.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

## أمثلة

يوضح كيفية تنسيق حقول FieldIndex.

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

### أنظر أيضا

* enum [FieldIndexFormat](../../fieldindexformat/)
* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
