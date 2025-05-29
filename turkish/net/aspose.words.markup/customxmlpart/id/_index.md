---
title: CustomXmlPart.Id
linktitle: Id
articleTitle: Id
second_title: .NET için Aspose.Words
description: Gelişmiş belge yönetimi için OOXML belgelerinizdeki XML parçalarını kolayca tanımlayıp özelleştirmek amacıyla CustomXmlPart Id özelliğini nasıl yöneteceğinizi keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.markup/customxmlpart/id/
---
## CustomXmlPart.Id property

Bu özel XML parçasını bir OOXML belgesi içinde tanımlayan dizeyi alır veya ayarlar.

```csharp
public string Id { get; set; }
```

## Notlar

ISO/IEC 29500 bu değerin bir GUID olduğunu belirtir, ancak Microsoft Word'ün eski sürümleri burada any dizesine izin veriyordu. Aspose.Words aynısını ECMA-376 biçimi için yapar. Ancak Microsoft Word Online'ın GUID olmayan bir değerle oluşturulmuş bir belgeyi açmak için 'yi başaramadığını unutmayın. Bu nedenle, bir GUID bu özellik için tercih edilen değerdir.

Geçerli bir değer, bu belgedeki tüm özel XML veri parçaları arasında benzersiz olan bir tanımlayıcı olmalıdır.

Varsayılan değer boş bir dizedir. Değer şu şekilde olamaz:`hükümsüz`.

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

* class [CustomXmlPart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
