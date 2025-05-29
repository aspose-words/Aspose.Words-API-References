---
title: XmlMapping.IsMapped
linktitle: IsMapped
articleTitle: IsMapped
second_title: .NET için Aspose.Words
description: XmlMapping IsMapped özelliğinin yapılandırılmış belgeler için XML veri eşlemesini nasıl etkili bir şekilde doğruladığını, sorunsuz entegrasyon ve doğruluğu nasıl sağladığını keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.markup/xmlmapping/ismapped/
---
## XmlMapping.IsMapped property

Geri Döndürür`doğru` eğer üst yapılandırılmış belge etiketi XML verilerine başarıyla eşlenirse.

```csharp
public bool IsMapped { get; }
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
