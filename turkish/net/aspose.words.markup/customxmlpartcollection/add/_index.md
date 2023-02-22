---
title: CustomXmlPartCollection.Add
second_title: Aspose.Words for .NET API Referansı
description: CustomXmlPartCollection yöntem. Koleksiyona bir öğe ekler.
type: docs
weight: 40
url: /tr/net/aspose.words.markup/customxmlpartcollection/add/
---
## Add(CustomXmlPart) {#add_1}

Koleksiyona bir öğe ekler.

```csharp
public void Add(CustomXmlPart part)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| part | CustomXmlPart | Eklenecek özel XML bölümü. |

### Örnekler

Özel XML verileriyle yapılandırılmış bir belge etiketinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Veri içeren bir XML parçası oluşturun ve bunu belgenin koleksiyonuna ekleyin.
// Microsoft Word'de "Geliştirici" sekmesini etkinleştirirsek,
// Bu koleksiyondaki öğeleri, birkaç varsayılan öğeyle birlikte "XML Eşleme Panosu"nda bulabiliriz.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Aşağıda, XML bölümlerine başvurmanın iki yolu vardır.
// 1 - Özel XML parça koleksiyonundaki bir dizine göre:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - GUID ile:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Bir XML şeması ilişkilendirmesi ekleyin.
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

// XML parça koleksiyonunu klonlayın ve ardından tüm öğelerini bir kerede kaldırmak için "Temizle" yöntemini kullanın.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Parçamızın içeriğini gösterecek ve onu belge gövdesine ekleyecek yapılandırılmış bir belge etiketi oluşturun.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Ayrıca bakınız

* class [CustomXmlPart](../../customxmlpart/)
* class [CustomXmlPartCollection](../)
* ad alanı [Aspose.Words.Markup](../../customxmlpartcollection/)
* toplantı [Aspose.Words](../../../)

---

## Add(string, string) {#add}

Belirtilen XML ile yeni bir XML bölümü oluşturur ve onu koleksiyona ekler.

```csharp
public CustomXmlPart Add(string id, string xml)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| id | String | Yeni bir özel XML bölümünün tanımlayıcısı. |
| xml | String | Parçanın XML verileri. |

### Geri dönüş değeri

Özel XML bölümü oluşturuldu.

### Örnekler

Özel XML verileriyle yapılandırılmış bir belge etiketinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Veri içeren bir XML parçası oluşturun ve bunu belgenin koleksiyonuna ekleyin.
// Microsoft Word'de "Geliştirici" sekmesini etkinleştirirsek,
// Bu koleksiyondaki öğeleri, birkaç varsayılan öğeyle birlikte "XML Eşleme Panosu"nda bulabiliriz.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Aşağıda, XML bölümlerine başvurmanın iki yolu vardır.
// 1 - Özel XML parça koleksiyonundaki bir dizine göre:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - GUID ile:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Bir XML şeması ilişkilendirmesi ekleyin.
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

// XML parça koleksiyonunu klonlayın ve ardından tüm öğelerini bir kerede kaldırmak için "Temizle" yöntemini kullanın.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Parçamızın içeriğini gösterecek ve onu belge gövdesine ekleyecek yapılandırılmış bir belge etiketi oluşturun.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Ayrıca bakınız

* class [CustomXmlPart](../../customxmlpart/)
* class [CustomXmlPartCollection](../)
* ad alanı [Aspose.Words.Markup](../../customxmlpartcollection/)
* toplantı [Aspose.Words](../../../)


