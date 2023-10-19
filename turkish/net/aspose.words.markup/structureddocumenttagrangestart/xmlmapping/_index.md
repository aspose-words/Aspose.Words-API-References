---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words for .NET
description: StructuredDocumentTagRangeStart XmlMapping mülk. Bu yapılandırılmış belge etiketi aralığının geçerli belgenin özel bir XML bölümündeki XML data ile eşlenmesini temsil eden bir nesne alır C#'da.
type: docs
weight: 180
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

Bu yapılandırılmış belge etiketi aralığının, geçerli belgenin özel bir XML bölümündeki XML data ile eşlenmesini temsil eden bir nesne alır.

```csharp
public XmlMapping XmlMapping { get; }
```

## Notlar

Kullanabilirsiniz[`SetMapping`](../../xmlmapping/setmapping/) yapılandırılmış bir belge etiketi aralığını XML verileriyle eşlemek için this nesnesinin yöntemi.

## Örnekler

Yapılandırılmış bir belge etiketinin aralık başlangıcı için XML eşlemelerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// Metin içeren bir XML parçası oluşturun ve bunu belgenin CustomXmlPart koleksiyonuna ekleyin.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// CustomXmlPart'ımızın içeriğini belgede görüntüleyecek yapılandırılmış bir belge etiketi oluşturun.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// Yapılandırılmış belge etiketimiz için bir eşleme ayarlarsak,
// CustomXmlPart'ın yalnızca XPath'ın işaret ettiği bir kısmını görüntüleyecektir.
// Bu XPath ikinci "<text>" içeriğine işaret edecek ilk "<root>" öğesinin öğesi CustomXmlPart'ımızın öğesi.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### Ayrıca bakınız

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
