---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: .NET için Aspose.Words
description: Daha iyi yönetim ve organizasyon için DOC dosyalarınızda saklanan belge sürümlerinin sayısını kolayca takip etmek amacıyla Document VersionsCount özelliğini keşfedin.
type: docs
weight: 480
url: /tr/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

DOC belgesinde saklanan belge sürümlerinin sayısını alır.

```csharp
public int VersionsCount { get; }
```

## Notlar

Microsoft Word'deki sürümlere Dosya/Sürümler menüsü üzerinden erişilir. Microsoft Word yalnızca DOC dosyaları için sürümlerini destekler.

Bu özellik, Aspose.Words'de açılmadan önce bu document içinde belge sürümlerinin depolanıp depolanmadığını algılamaya olanak tanır. Aspose.Words, belge sürümleri için başka bir destek sağlamaz. Bu belgeyi Aspose.Words kullanarak kaydederseniz, belge sürümler olmadan kaydedilir.

## Örnekler

Eski Microsoft Word belgelerinin sürüm sayma özelliğinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// Bir belgenin bu özelliğini okuyabiliriz, ancak kaydederken bunu koruyamayız.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
