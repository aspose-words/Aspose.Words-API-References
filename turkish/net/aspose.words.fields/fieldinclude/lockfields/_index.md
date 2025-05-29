---
title: FieldInclude.LockFields
linktitle: LockFields
articleTitle: LockFields
second_title: .NET için Aspose.Words
description: FieldInclude LockFields özelliğiyle belge güncellemelerini zahmetsizce yönetin. Alan düzenlemeyi kontrol edin ve belge bütünlüğünü kolaylıkla geliştirin.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldinclude/lockfields/
---
## FieldInclude.LockFields property

Dahil edilen belgedeki alanların güncellenmesinin engellenip engellenmeyeceğini alır veya ayarlar.

```csharp
public bool LockFields { get; set; }
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
