---
title: SourceFullName
second_title: Aspose.Words for .NET API Referansı
description: Belgenin konumunu alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldinclude/sourcefullname/
---
## FieldInclude.SourceFullName property

Belgenin konumunu alır veya ayarlar.

```csharp
public string SourceFullName { get; set; }
```

### Örnekler

INCLUDE alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sisteminde başka bir belgenin bir bölümünü içe aktarmak için bir INCLUDE alanını kullanabiliriz.
// Bu alanla referans verdiğimiz diğer belgedeki yer imi, içe aktarılan bu kısmı içerir.
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

* class [FieldInclude](../../fieldinclude)
* ad alanı [Aspose.Words.Fields](../../fieldinclude)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
