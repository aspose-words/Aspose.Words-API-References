---
title: CustomXmlPartCollection Class
linktitle: CustomXmlPartCollection
articleTitle: CustomXmlPartCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Markup.CustomXmlPartCollection sınıf. Özel XML Parçalarının bir koleksiyonunu temsil eder. ÖğelerCustomXmlPart nesneler C#'da.
type: docs
weight: 3930
url: /tr/net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

Özel XML Parçalarının bir koleksiyonunu temsil eder. Öğeler[`CustomXmlPart`](../customxmlpart/) nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokümantasyon makalesi.

```csharp
public class CustomXmlPartCollection : IEnumerable<CustomXmlPart>
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CustomXmlPartCollection](customxmlpartcollection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpartcollection/count/) { get; } | Koleksiyonda yer alan öğelerin sayısını alır. |
| [Item](../../aspose.words.markup/customxmlpartcollection/item/) { get; set; } | Belirtilen dizindeki bir öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add_1)(*[CustomXmlPart](../customxmlpart/)*) | Koleksiyona bir öğe ekler. |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add)(*string, string*) | Belirtilen XML ile yeni bir XML parçası oluşturur ve bunu koleksiyona ekler. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone/)() | Bu koleksiyonun ve içindeki öğelerin derin bir kopyasını oluşturur. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid/)(*string*) | Özel bir XML parçasını tanımlayıcısına göre bulur ve döndürür. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat/)(*int*) | Belirtilen dizindeki bir öğeyi kaldırır. |

## Notlar

Normalde bu sınıfın örneklerini oluşturmanıza gerek yoktur. Bir belgede saklanan özel XML verilerine erişebilirsiniz.[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) mülk.

## Örnekler

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

* class [CustomXmlPart](../customxmlpart/)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
