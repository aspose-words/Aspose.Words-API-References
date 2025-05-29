---
title: DocumentProperty.ToInt
linktitle: ToInt
articleTitle: ToInt
second_title: .NET için Aspose.Words
description: ToInt metoduyla DocumentProperty değerlerini zahmetsizce tam sayılara dönüştürün. Uygulamalarınız için kusursuz veri işlemeyi açığa çıkarın!
type: docs
weight: 100
url: /tr/net/aspose.words.properties/documentproperty/toint/
---
## DocumentProperty.ToInt method

Özellik değerini tam sayı olarak döndürür.

```csharp
public int ToInt()
```

## Notlar

Özellik türü uygun değilse bir istisna atarNumber .

## Örnekler

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
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
