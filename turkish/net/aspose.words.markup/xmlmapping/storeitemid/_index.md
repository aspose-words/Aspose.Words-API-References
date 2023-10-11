---
title: XmlMapping.StoreItemId
second_title: Aspose.Words for .NET API Referansı
description: XmlMapping mülk. Özel XML veri kısmı için özel XML veri tanımlayıcısını belirtir ve bu parçanın değerlendirilmesinde kullanılır.XPath ifade.
type: docs
weight: 40
url: /tr/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Özel XML veri kısmı için özel XML veri tanımlayıcısını belirtir ve bu parçanın değerlendirilmesinde kullanılır.[`XPath`](../xpath/) ifade.

```csharp
public string StoreItemId { get; }
```

### Örnekler

Bir XML bölümünün özel XML veri tanımlayıcısının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// Yapılandırılmış belge etiketlerinin GUID biçiminde kimlikleri vardır.
StructuredDocumentTag tag = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### Ayrıca bakınız

* class [XmlMapping](../)
* ad alanı [Aspose.Words.Markup](../../xmlmapping/)
* toplantı [Aspose.Words](../../../)


