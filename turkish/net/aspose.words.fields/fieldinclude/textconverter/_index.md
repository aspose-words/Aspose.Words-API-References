---
title: FieldInclude.TextConverter
second_title: Aspose.Words for .NET API Referansı
description: FieldInclude mülk. Dahil edilen dosyanın biçimi için metin dönüştürücünün adını alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldinclude/textconverter/
---
## FieldInclude.TextConverter property

Dahil edilen dosyanın biçimi için metin dönüştürücünün adını alır veya ayarlar.

```csharp
public string TextConverter { get; set; }
```

### Örnekler

INCLUDE alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sistemine başka bir belgenin bir bölümünü içe aktarmak için INCLUDE alanını kullanabiliriz.
// Bu alanla referans verdiğimiz diğer belgedeki yer imi bu içe aktarılan kısmı içeriyor.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### Ayrıca bakınız

* class [FieldInclude](../)
* ad alanı [Aspose.Words.Fields](../../fieldinclude/)
* toplantı [Aspose.Words](../../../)


