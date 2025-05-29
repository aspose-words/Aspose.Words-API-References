---
title: CompareOptions.AdvancedOptions
linktitle: AdvancedOptions
articleTitle: AdvancedOptions
second_title: .NET için Aspose.Words
description: Karşılaştırmalarınızı geliştirmek için CompareOptions AdvancedOptions'ı keşfedin. En iyi çıktı için özel ayarlarla hassas sonuçlar elde edin.
type: docs
weight: 20
url: /tr/net/aspose.words.comparing/compareoptions/advancedoptions/
---
## CompareOptions.AdvancedOptions property

Daha kesin karşılaştırma çıktısı üretmeye yardımcı olabilecek gelişmiş karşılaştırma seçeneklerini belirtir.

```csharp
public AdvancedCompareOptions AdvancedOptions { get; }
```

## Örnekler

DML benzersiz kimliğini göz ardı ederek belgelerin nasıl karşılaştırılacağını gösterir.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Varsayılan olarak, Aspose.Words DML'nin benzersiz kimliğini yok saymaz ve revizyon sayısı 2'dir.
// DML'nin benzersiz kimliğini göz ardı edersek ve revizyon sayısı 0 ise.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Ayrıca bakınız

* class [AdvancedCompareOptions](../../advancedcompareoptions/)
* class [CompareOptions](../)
* ad alanı [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../../)
