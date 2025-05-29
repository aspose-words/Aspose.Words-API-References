---
title: FieldInclude.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: .NET için Aspose.Words
description: Belge konumlarını verimli bir şekilde yönetmek için FieldInclude SourceFullName özelliğini nasıl kullanacağınızı keşfedin. İş akışınızı bugün geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldinclude/sourcefullname/
---
## FieldInclude.SourceFullName property

Belgenin konumunu alır veya ayarlar.

```csharp
public string SourceFullName { get; set; }
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
