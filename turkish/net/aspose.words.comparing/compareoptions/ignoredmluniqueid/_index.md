---
title: CompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words for .NET
description: CompareOptions IgnoreDmlUniqueId mülk. DrawingML benzersiz kimliğindeki farkın göz ardı edilip edilmeyeceğini belirtir. Varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

DrawingML benzersiz kimliğindeki farkın göz ardı edilip edilmeyeceğini belirtir. Varsayılan değer:`YANLIŞ` .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## Örnekler

DML benzersiz kimliğini göz ardı ederek belgelerin nasıl karşılaştırılacağını gösterir.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Varsayılan olarak Aspose.Words, DML'nin benzersiz kimliğini göz ardı etmez ve revizyon sayısı 2'dir.
// DML'nin benzersiz kimliğini göz ardı ediyorsak ve revizyon sayısı 0 ise.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Ayrıca bakınız

* class [CompareOptions](../)
* ad alanı [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../../)
