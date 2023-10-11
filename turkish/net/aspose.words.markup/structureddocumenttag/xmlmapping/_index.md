---
title: StructuredDocumentTag.XmlMapping
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTag mülk. Bu yapılandırılmış belge etiketinin geçerli belgenin özel bir XML bölümündeki XML data ile eşlenmesini temsil eden bir nesne alır.
type: docs
weight: 320
url: /tr/net/aspose.words.markup/structureddocumenttag/xmlmapping/
---
## StructuredDocumentTag.XmlMapping property

Bu yapılandırılmış belge etiketinin, geçerli belgenin özel bir XML bölümündeki XML data ile eşlenmesini temsil eden bir nesne alır.

```csharp
public XmlMapping XmlMapping { get; }
```

### Notlar

Kullanabilirsiniz[`SetMapping`](../../xmlmapping/setmapping/) bu nesnenin yöntemini XML verilerine eşlemek için yapılandırılmış bir belge etiketi.

### Örnekler

Özel XML verileriyle yapılandırılmış bir belge etiketinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Veri içeren bir XML bölümü oluşturun ve onu belgenin koleksiyonuna ekleyin.
// Microsoft Word'de "Geliştirici" sekmesini etkinleştirirsek,
// bu koleksiyondaki öğeleri birkaç varsayılan öğeyle birlikte "XML Eşleme Bölmesi"nde bulabiliriz.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Aşağıda XML parçalarına başvurmanın iki yolu verilmiştir.
// 1 - Özel XML parça koleksiyonundaki bir dizine göre:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - GUID'e göre:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Bir XML şeması ilişkisi ekleyin.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Bir parçayı klonlayın ve ardından onu koleksiyona ekleyin.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Koleksiyonu yineleyin ve her parçanın içeriğini yazdırın.
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// Klonlanan parçayı dizine göre kaldırmak için "RemoveAt" yöntemini kullanın.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// XML parça koleksiyonunu kopyalayın ve ardından tüm öğelerini bir kerede kaldırmak için "Temizle" yöntemini kullanın.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Parçamızın içeriğini görüntüleyecek yapılandırılmış bir belge etiketi oluşturun ve bunu belge gövdesine ekleyin.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Ayrıca bakınız

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttag/)
* toplantı [Aspose.Words](../../../)


