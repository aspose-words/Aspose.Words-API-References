---
title: Class XmlMapping
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Markup.XmlMapping sınıf. parent yapılandırılmış belge etiketi ile belgedeki özel bir XML veri bölümünde depolanan bir XML öğesi arasında eşleme oluşturmak için kullanılan bilgiyi belirtir.
type: docs
weight: 4100
url: /tr/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

parent yapılandırılmış belge etiketi ile belgedeki özel bir XML veri bölümünde depolanan bir XML öğesi arasında eşleme oluşturmak için kullanılan bilgiyi belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokümantasyon makalesi.

```csharp
public class XmlMapping
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Üst yapılandırılmış belge etiketinin eşlendiği özel XML veri bölümünü döndürür. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | İadeler`doğru` ana yapılandırılmış belge etiketi XML verileriyle başarıyla eşlendiyse. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Değerlendirmek için XML ad alanı öneki eşlemelerini döndürür[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Özel XML veri kısmı için özel XML veri tanımlayıcısını belirtir ve bu parçanın değerlendirilmesinde kullanılır.[`XPath`](./xpath/) ifade. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Üst yapılandırılmış belge etiketiyle eşlenen özel XML node 'yi bulmak için değerlendirilen XPath ifadesini döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Ana yapılandırılmış belgenin XML verileriyle eşlenmesini siler. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(CustomXmlPart, string, string) | Ana yapılandırılmış belge etiketi ile özel bir XML veri bölümünün XML düğümü arasında bir eşleme ayarlar. |

### Örnekler

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

// Yapılandırılmış belge etiketimiz için bir eşleme ayarlayın. Bu haritalama talimat verecek
// XPath'ın işaret ettiği XML bölümünün metin içeriğinin bir kısmını görüntülemek için yapılandırılmış belge etiketimiz.
// Bu durumda, ikinci "<text>" içeriği olacaktır. ilk "<root>" öğesinin öğesi öğe: "Metin öğesi #2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.XmlMapping.PrefixMappings);

// Özel bölümümüzdeki içeriği görüntülemek için yapılandırılmış belge etiketini belgeye ekleyin.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)


