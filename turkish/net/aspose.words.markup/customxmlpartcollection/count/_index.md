---
title: CustomXmlPartCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: Gelişmiş veri yönetimi için XML koleksiyonunuzdaki toplam öğe sayısını kolayca almak üzere CustomXmlPartCollection Count özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.markup/customxmlpartcollection/count/
---
## CustomXmlPartCollection.Count property

Koleksiyonda bulunan öğelerin sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Özel XML verileriyle yapılandırılmış bir belge etiketinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Veri içeren bir XML parçası oluştur ve bunu belgenin koleksiyonuna ekle.
// Microsoft Word'de "Geliştirici" sekmesini etkinleştirirsek,
// Bu koleksiyondaki öğeleri "XML Eşleme Bölmesi"nde, birkaç varsayılan öğeyle birlikte bulabiliriz.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Aşağıda XML parçalarına başvurmanın iki yolu bulunmaktadır.
// 1 - Özel XML parça koleksiyonundaki bir dizine göre:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - GUID'e göre:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Bir XML şema ilişkisi ekleyin.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Bir parçayı klonla ve sonra onu koleksiyona ekle.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Koleksiyonda gezinin ve her parçanın içeriğini yazdırın.
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

// Klonlanmış parçayı indekse göre kaldırmak için "RemoveAt" metodunu kullanın.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// XML parça koleksiyonunu kopyalayın ve ardından tüm öğelerini bir kerede kaldırmak için "Clear" yöntemini kullanın.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Parçamızın içeriğini görüntüleyecek yapılandırılmış bir belge etiketi oluşturup bunu belge gövdesine ekleyelim.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Ayrıca bakınız

* class [CustomXmlPartCollection](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
