---
title: XmlMapping.PrefixMappings
linktitle: PrefixMappings
articleTitle: PrefixMappings
second_title: .NET için Aspose.Words
description: Kusursuz XML ad alanı ön eki eşlemesi ve verimli XPath değerlendirmesi için XmlMapping PrefixMappings özelliğini keşfedin. XML işlemenizi bugün geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.markup/xmlmapping/prefixmappings/
---
## XmlMapping.PrefixMappings property

XML ad alanı öneki eşlemelerini değerlendirecek şekilde döndürür[`XPath`](../xpath/) .

```csharp
public string PrefixMappings { get; }
```

## Notlar

XPath ifadesi belgedeki özel XML veri parçalarına göre değerlendirildiğinde XPath ifadesinin yorumlanmasında kullanılacak önek eşlemeleri kümesini belirtir.

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
