---
title: CompareOptions.IgnoreDmlUniqueId
second_title: Aspose.Words for .NET API Referansı
description: CompareOptions mülk. DrawingML benzersiz kimliğindeki farkın yoksayılıp yoksayılmayacağını belirtir. Varsayılan değer yanlış .
type: docs
weight: 50
url: /tr/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

DrawingML benzersiz kimliğindeki farkın yoksayılıp yoksayılmayacağını belirtir. Varsayılan değer **yanlış** .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

### Örnekler

DML benzersiz kimliğini yok sayarak belgelerin nasıl karşılaştırılacağını gösterir.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Varsayılan olarak Aspose.Words, DML'nin benzersiz kimliğini göz ardı etmez ve revizyon sayısı 2'dir.
// DML'nin benzersiz kimliğini görmezden geliyorsak ve revizyon sayısı 0 idi.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Ayrıca bakınız

* class [CompareOptions](../)
* ad alanı [Aspose.Words.Comparing](../../compareoptions/)
* toplantı [Aspose.Words](../../../)


