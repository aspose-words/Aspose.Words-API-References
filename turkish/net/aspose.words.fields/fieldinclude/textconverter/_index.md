---
title: FieldInclude.TextConverter
linktitle: TextConverter
articleTitle: TextConverter
second_title: .NET için Aspose.Words
description: FieldInclude TextConverter özelliğini keşfedin; gelişmiş iş akışı verimliliği için özelleştirilebilir metin dönüştürücü adlarıyla dosya biçimi dönüşümlerini kolayca yönetin.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldinclude/textconverter/
---
## FieldInclude.TextConverter property

Dahil edilen dosyanın biçimi için metin dönüştürücünün adını alır veya ayarlar.

```csharp
public string TextConverter { get; set; }
```

## Örnekler

INCLUDE alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sistemindeki başka bir belgenin bir kısmını içe aktarmak için INCLUDE alanını kullanabiliriz.
// Bu alanla başvurduğumuz diğer belgedeki yer imi bu içe aktarılan kısmı içerir.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
