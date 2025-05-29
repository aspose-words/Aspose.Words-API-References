---
title: AdvancedCompareOptions Class
linktitle: AdvancedCompareOptions
articleTitle: AdvancedCompareOptions
second_title: .NET için Aspose.Words
description: Güçlü belge karşılaştırması için Aspose.Words.AdvancedCompareOptions sınıfını keşfedin. Hassas sonuçlar ve gelişmiş üretkenlik için ayarları özelleştirin.
type: docs
weight: 460
url: /tr/net/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class

Gelişmiş karşılaştırma seçeneklerinin ayarlanmasına izin verir.

```csharp
public class AdvancedCompareOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [AdvancedCompareOptions](advancedcompareoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/) { get; set; } | DrawingML benzersiz kimliğindeki farkın göz ardı edilip edilmeyeceğini belirtir. |
| [IgnoreStoreItemId](../../aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/) { get; set; } | StructuredDocumentTag depolama öğesi kimliğindeki farkın göz ardı edilip edilmeyeceğini belirtir. |

## Notlar

Bu seçeneklerin Microsoft Word'de karşılığı yoktur ve daha kesin karşılaştırma sonucu üretmeye yardımcı olabilir.

## Örnekler

Aynı içeriğe sahip ancak farklı mağaza öğesi kimliğine sahip SDT'nin nasıl karşılaştırılacağını gösterir.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Aynı içeriğe sahip ancak farklı mağaza öğesi kimliğine sahip SDT'yi karşılaştırmak için seçenekleri yapılandırın.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Comparing](../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../)
