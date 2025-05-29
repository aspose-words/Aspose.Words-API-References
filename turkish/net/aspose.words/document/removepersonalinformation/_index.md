---
title: Document.RemovePersonalInformation
linktitle: RemovePersonalInformation
articleTitle: RemovePersonalInformation
second_title: .NET için Aspose.Words
description: Word'deki Belge Kişisel Bilgileri Kaldır özelliğiyle gizliliğinizi koruyun; kaydettiğinizde kullanıcı verilerini yorumlar ve özelliklerden otomatik olarak silin.
type: docs
weight: 360
url: /tr/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Microsoft Word'ün belgeyi kaydederken tüm kullanıcı bilgilerini yorumlardan, düzeltmelerden ve belge özelliklerinden kaldıracağını belirten bir bayrak alır veya ayarlar.

```csharp
public bool RemovePersonalInformation { get; set; }
```

## Örnekler

Manuel kaydetme sırasında kişisel bilgilerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kişisel bilgilerinizin yer aldığı bir içerik ekleyin.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// Bu bayrak, Dosya -> Seçenekler -> Güven Merkezi -> Güven Merkezi Ayarları... -> ile eşdeğerdir.
// Gizlilik Seçenekleri -> "Microsoft Word'de kaydederken dosya özelliklerinden kişisel bilgileri kaldır".
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// Bu seçenek Aspose.Words kullanılarak yapılan bir kaydetme işlemi sırasında etkili olmayacaktır.
// Microsoft Word kullanarak manuel olarak kaydettiğimizde, bayrak ayarlı olarak kişisel veriler belgemizden kaldırılacaktır.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
