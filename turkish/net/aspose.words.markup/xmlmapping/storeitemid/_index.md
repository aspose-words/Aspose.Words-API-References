---
title: StoreItemId
second_title: Aspose.Words for .NET API Referansı
description: Özel XML veri bölümü için özel XML veri tanımlayıcısını belirtir ve bu öğesinin aşağıdakileri değerlendirmek için kullanılacaktır.XPathaspose.words.markup/xmlmapping/xpath ifade.
type: docs
weight: 40
url: /tr/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Özel XML veri bölümü için özel XML veri tanımlayıcısını belirtir ve bu, öğesinin aşağıdakileri değerlendirmek için kullanılacaktır.[`XPath`](../xpath) ifade.

```csharp
public string StoreItemId { get; }
```

### Örnekler

Bir XML parçasının özel XML veri tanımlayıcısının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// Yapılandırılmış belge etiketlerinin GUID biçiminde kimlikleri vardır.
StructuredDocumentTag tag = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### Ayrıca bakınız

* class [XmlMapping](../../xmlmapping)
* ad alanı [Aspose.Words.Markup](../../xmlmapping)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
