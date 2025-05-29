---
title: FieldIndexFormat Enum
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: .NET için Aspose.Words
description: Belgelerinizde özelleştirilebilir FieldIndex biçimlendirmesi için Aspose.Words.FieldIndexFormat enum'ını keşfedin. Belgenizin yapısını zahmetsizce geliştirin!
type: docs
weight: 2480
url: /tr/net/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enumeration

Biçimlendirmeyi belirtir[`FieldIndex`](../fieldindex/) bir belgedeki alanlar.

```csharp
public enum FieldIndexFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Template | `0` | Şablondan. |
| Classic | `1` | Klasik. |
| Fancy | `2` | Süslü. |
| Modern | `3` | Modern. |
| Bulleted | `4` | Madde işaretli. |
| Formal | `5` | Resmi. |
| Simple | `6` | Basit. |

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

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
