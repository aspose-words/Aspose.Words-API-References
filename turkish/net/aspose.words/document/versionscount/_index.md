---
title: Document.VersionsCount
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. DOC belgesinde saklanan belge sürümlerinin sayısını alır.
type: docs
weight: 460
url: /tr/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

DOC belgesinde saklanan belge sürümlerinin sayısını alır.

```csharp
public int VersionsCount { get; }
```

### Notlar

Microsoft Word'deki sürümlere Dosya/Sürümler menüsünden erişilir. Microsoft Word sürümlerini yalnızca DOC dosyaları için destekler.

Bu özellik, Aspose.Words'de açılmadan önce bu document dosyasında saklanan belge sürümlerinin olup olmadığının tespit edilmesine olanak tanır. Aspose.Words, belge sürümleri için başka bir destek sağlamaz. Bu belgeyi Aspose.Words kullanarak kaydederseniz, belge sürümler olmadan kaydedilir.

### Örnekler

Eski Microsoft Word belgelerinin sürüm sayımı özelliğiyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// Bir belgenin bu özelliğini okuyabiliyoruz ancak kaydederken koruyamayız.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");      
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


