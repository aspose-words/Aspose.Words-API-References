---
title: FieldToc.CaptionlessTableOfFiguresLabel
linktitle: CaptionlessTableOfFiguresLabel
articleTitle: CaptionlessTableOfFiguresLabel
second_title: .NET için Aspose.Words
description: Şekil tablonuzu özelleştirmek için FieldToc CaptionlessTableOfFiguresLabel özelliğini keşfedin. Başlıklar olmadan dizi tanımlayıcılarını kolayca yönetin!
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/
---
## FieldToc.CaptionlessTableOfFiguresLabel property

Başlık etiketi ve numarasını içermeyen bir şekil tablosu oluştururken kullanılan sıra tanımlayıcısının adını alır veya ayarlar.

```csharp
public string CaptionlessTableOfFiguresLabel { get; set; }
```

## Örnekler

Sıra tanımlayıcısının adının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);
fieldToc.CaptionlessTableOfFiguresLabel = "Test";

Assert.AreEqual(" TOC  \\a Test", fieldToc.GetFieldCode());
```

### Ayrıca bakınız

* class [FieldToc](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
