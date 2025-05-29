---
title: AdvancedCompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: .NET için Aspose.Words
description: Benzersiz kimlikleri verimli bir şekilde yöneterek DrawingML işlemenizi geliştirmek için AdvancedCompareOptions IgnoreDmlUniqueId özelliğini keşfedin. İş akışınızı optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/
---
## AdvancedCompareOptions.IgnoreDmlUniqueId property

DrawingML benzersiz kimliğindeki farkın göz ardı edilip edilmeyeceğini belirtir.

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## Notlar

Varsayılan değer`YANLIŞ` .

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

* class [AdvancedCompareOptions](../)
* ad alanı [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../../)
