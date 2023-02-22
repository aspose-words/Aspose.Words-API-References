---
title: FieldOptions.FieldIndexFormat
second_title: Aspose.Words لمراجع .NET API
description: FieldOptions ملكية. يحصل أو يحدد أFieldIndexFormat الذي يمثل تنسيق ملفFieldIndexالحقول في المستند.
type: docs
weight: 80
url: /ar/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

يحصل أو يحدد أ`FieldIndexFormat` الذي يمثل تنسيق ملف[`FieldIndex`](../../fieldindex/)الحقول في المستند.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words.Fields](../../fieldoptions/)
* المجسم [Aspose.Words](../../../)


