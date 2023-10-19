---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words for .NET
description: MailMerge TrimWhitespaces mülk. Adresmektup birleştirme değerlerinden sondaki ve baştaki boşlukların kırpılıp kırpılmadığını belirten bir değer alır veya ayarlar C#'da.
type: docs
weight: 130
url: /tr/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Adres-mektup birleştirme değerlerinden sondaki ve baştaki boşlukların kırpılıp kırpılmadığını belirten bir değer alır veya ayarlar.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Notlar

Varsayılan değer:`doğru` .

## Örnekler

Adres-mektup birleştirme yürütülürken bir veri kaynağının değerlerindeki boşlukların nasıl kırpılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("MERGEFIELD myMergeField", null);

doc.MailMerge.TrimWhitespaces = trimWhitespaces;
doc.MailMerge.Execute(new[] { "myMergeField" }, new object[] { "\t hello world! " });

Assert.AreEqual(trimWhitespaces ? "hello world!\f" : "\t hello world! \f", doc.GetText());
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
