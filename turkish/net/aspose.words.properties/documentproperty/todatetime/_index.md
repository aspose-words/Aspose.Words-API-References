---
title: DocumentProperty.ToDateTime
second_title: Aspose.Words for .NET API Referansı
description: DocumentProperty yöntem. Özellik değerini UTCde DateTime olarak döndürür.
type: docs
weight: 80
url: /tr/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

Özellik değerini UTC'de DateTime olarak döndürür.

```csharp
public DateTime ToDateTime()
```

### Notlar

Özellik türü değilse bir istisna atarDateTime.

Microsoft Word, özel tarih özellikleri için yalnızca tarih bölümünü (saat yok) depolar.

### Örnekler

Tarih ve saat içeren özel bir belge özelliğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

Özel belge özelliklerinin çeşitli tür dönüştürme yöntemlerini gösterir.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

### Ayrıca bakınız

* class [DocumentProperty](../)
* ad alanı [Aspose.Words.Properties](../../documentproperty/)
* toplantı [Aspose.Words](../../../)


