---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: .NET için Aspose.Words
description: StructuredDocumentTagRangeStart XmlMapping özelliğinin belgenizin etiket aralığını özel XML verilerine nasıl bağlayarak belge bütünleşmesini geliştirdiğini keşfedin.
type: docs
weight: 190
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

Bu yapılandırılmış belge etiketi aralığının, geçerli belgenin özel bir XML bölümündeki XML data eşlemesini temsil eden bir nesne alır.

```csharp
public XmlMapping XmlMapping { get; }
```

## Notlar

Şunu kullanabilirsiniz:[`SetMapping`](../../xmlmapping/setmapping/) this nesnesinin yapılandırılmış bir belge etiketi aralığını XML verilerine eşleme yöntemi.

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

// Belgede CustomXmlPart'ımızın içeriğini görüntüleyecek yapılandırılmış bir belge etiketi oluşturun.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// Yapılandırılmış belge etiketimiz için bir eşleme ayarlarsak,
// yalnızca XPath'nin işaret ettiği CustomXmlPart'ın bir kısmını görüntüler.
// Bu XPath, CustomXmlPart'ımızın ilk "<root>" öğesinin ikinci "<text>" öğesinin içeriğine işaret edecektir.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### Ayrıca bakınız

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
