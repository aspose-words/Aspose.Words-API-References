---
title: FieldOptions.FieldIndexFormat
second_title: Aspose.Words for .NET API Referansı
description: FieldOptions mülk. Bir değeri alır veya ayarlarFieldIndexFormat bu biçimlendirmeyi temsil ederFieldIndex belgedeki alanlar.
type: docs
weight: 90
url: /tr/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

Bir değeri alır veya ayarlar`FieldIndexFormat` bu, biçimlendirmeyi temsil eder[`FieldIndex`](../../fieldindex/) belgedeki alanlar.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

### Örnekler

FieldIndex alanlarının nasıl biçimlendirileceğini gösterir.

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

### Ayrıca bakınız

* enum [FieldIndexFormat](../../fieldindexformat/)
* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../fieldoptions/)
* toplantı [Aspose.Words](../../../)


