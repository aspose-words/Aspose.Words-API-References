---
title: FieldOptions.FieldIndexFormat
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية الاستفادة من خاصية FieldIndexFormat في FieldOptions لتخصيص تنسيق FieldIndex لتحسين وضوح المستند وتنظيمه.
type: docs
weight: 90
url: /ar/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

يحصل على أو يعين`FieldIndexFormat` الذي يمثل التنسيق لـ[`FieldIndex`](../../fieldindex/) الحقول في المستند.

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
