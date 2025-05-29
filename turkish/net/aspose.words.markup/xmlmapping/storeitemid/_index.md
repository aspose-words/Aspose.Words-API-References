---
title: XmlMapping.StoreItemId
linktitle: StoreItemId
articleTitle: StoreItemId
second_title: .NET için Aspose.Words
description: Özel XML veri tanımlayıcıları için XmlMapping StoreItemId özelliğini keşfedin. Verimli veri yönetimi için benzersiz çözümlerimizle XPath değerlendirmesini geliştirin.
type: docs
weight: 40
url: /tr/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Özel XML veri parçası için özel XML veri tanımlayıcısını belirtir. , bu tanımlayıcının değerlendirilmesinde kullanılacaktır.[`XPath`](../xpath/) ifade.

```csharp
public string StoreItemId { get; }
```

## Örnekler

Bir XML parçasının özel XML veri tanımlayıcısının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// Yapılandırılmış belge etiketlerinin GUID biçiminde kimlikleri vardır.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### Ayrıca bakınız

* class [XmlMapping](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
