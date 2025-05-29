---
title: FieldOptions.FieldIndexFormat
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: .NET için Aspose.Words
description: Gelişmiş belge netliği ve organizasyonu için FieldIndex biçimlendirmesini özelleştirmek amacıyla FieldOptions'daki FieldIndexFormat özelliğinin nasıl kullanılacağını keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

Bir değeri alır veya ayarlar`FieldIndexFormat` bu, x000d_ biçimlendirmesini temsil eder[`FieldIndex`](../../fieldindex/) belgedeki alanlar.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

## Örnekler

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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
