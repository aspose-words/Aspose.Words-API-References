---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: .NET için Aspose.Words
description: Belgenizin veri bütünleşmesini geliştirerek yapılandırılmış belge etiketlerini XML öğeleriyle sorunsuz bir şekilde bağlamak için Aspose.Words.Markup.XmlMapping sınıfını keşfedin.
type: docs
weight: 4790
url: /tr/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Parent yapılandırılmış belge etiketi ile belgedeki özel XML veri parçasında depolanan bir XML öğesi arasında bir eşleme kurmak için kullanılan bilgileri belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

```csharp
public class XmlMapping
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Üst yapılandırılmış belge etiketinin eşlendiği özel XML veri bölümünü döndürür. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Geri Döndürür`doğru` eğer üst yapılandırılmış belge etiketi XML verilerine başarıyla eşlenirse. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | XML ad alanı öneki eşlemelerini değerlendirecek şekilde döndürür[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Özel XML veri parçası için özel XML veri tanımlayıcısını belirtir. , bu tanımlayıcının değerlendirilmesinde kullanılacaktır.[`XPath`](./xpath/) ifade. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Üst yapılandırılmış belge etiketine eşlenen özel XML düğümünü bulmak için değerlendirilen XPath ifadesini döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Üst yapılandırılmış belgenin XML verilerine eşlenmesini siler. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | Üst yapılandırılmış belge etiketi ile özel bir XML veri parçasının XML düğümü arasında bir eşleme ayarlar. |

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

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
