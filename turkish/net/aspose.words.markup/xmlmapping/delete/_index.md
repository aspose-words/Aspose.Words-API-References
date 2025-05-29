---
title: XmlMapping.Delete
linktitle: Delete
articleTitle: Delete
second_title: .NET için Aspose.Words
description: XmlMapping Delete yöntemiyle XML veri eşlemelerini zahmetsizce kaldırın. Gelişmiş verimlilik ve organizasyon için yapılandırılmış belgelerinizi düzenleyin.
type: docs
weight: 60
url: /tr/net/aspose.words.markup/xmlmapping/delete/
---
## XmlMapping.Delete method

Üst yapılandırılmış belgenin XML verilerine eşlenmesini siler.

```csharp
public void Delete()
```

## Örnekler

Özel XML parçaları için XML eşlemelerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Metin içeren bir XML parçası oluşturun ve bunu belgenin CustomXmlPart koleksiyonuna ekleyin.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// CustomXmlPart'ımızın içeriğini görüntüleyecek yapılandırılmış bir belge etiketi oluşturun.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Yapılandırılmış belge etiketimiz için bir eşleme ayarlayın. Bu eşleme talimat verecektir
// XPath'ın işaret ettiği XML parçasının metin içeriğinin bir kısmını görüntülemek için yapılandırılmış belge etiketimiz.
// Bu durumda, ilk "<root>" öğesinin ikinci "<text>" öğesinin içeriği olacaktır: "Text element #2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", etiket.XmlMapping.PrefixMappings);

// Özel parçamızdaki içeriği görüntülemek için belgeye yapılandırılmış belge etiketini ekleyin.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Ayrıca bakınız

* class [XmlMapping](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
