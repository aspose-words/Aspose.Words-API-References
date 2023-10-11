---
title: Document.RemovePersonalInformation
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. Belgeyi kaydettikten sonra Microsoft Wordün yorumlardan düzeltmelerden ve belge özelliklerinden tüm kullanıcı bilgilerini kaldıracağını belirten bir işaret alır veya ayarlar.
type: docs
weight: 340
url: /tr/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Belgeyi kaydettikten sonra Microsoft Word'ün yorumlardan, düzeltmelerden ve belge özelliklerinden tüm kullanıcı bilgilerini kaldıracağını belirten bir işaret alır veya ayarlar.

```csharp
public bool RemovePersonalInformation { get; set; }
```

### Örnekler

Manuel kaydetme sırasında kişisel bilgilerin kaldırılmasının nasıl etkinleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kişisel bilgiler içeren bir miktar içerik ekleyin.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// Bu bayrak Dosya -> Seçenekler -> Güven Merkezi -> Güven Merkezi Ayarları... ->
// Gizlilik Seçenekleri -> Microsoft Word'de "Kayıt sırasında dosya özelliklerinden kişisel bilgileri kaldır".
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// Aspose.Words kullanılarak yapılan kaydetme işlemi sırasında bu seçenek etkili olmayacaktır.
// Microsoft Word kullanarak manuel olarak kaydettiğimizde kişisel veriler bayrak seti ile belgemizden kaldırılacaktır.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


