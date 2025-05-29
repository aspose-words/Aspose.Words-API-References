---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: .NET için Aspose.Words
description: TrimWhitespaces özelliğiyle posta birleştirme işleminizi optimize edin; doğru sonuçlar için baştaki ve sondaki boşlukları kaldırarak temiz veriler sağlayın.
type: docs
weight: 130
url: /tr/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Posta birleştirme değerlerinden son ve öndeki boşlukların kesilip kesilmeyeceğini belirten bir değer alır veya ayarlar.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Notlar

Varsayılan değer:`doğru` .

## Örnekler

Bir posta birleştirme işlemi yürütülürken bir veri kaynağının değerlerinden boşlukların nasıl kırpılacağını gösterir.

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
