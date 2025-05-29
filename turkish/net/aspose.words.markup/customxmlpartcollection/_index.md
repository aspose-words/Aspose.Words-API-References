---
title: CustomXmlPartCollection Class
linktitle: CustomXmlPartCollection
articleTitle: CustomXmlPartCollection
second_title: .NET için Aspose.Words
description: Özel XML Parçalarını verimli ve zahmetsizce yönetmek için başvuracağınız çözüm olan Aspose.Words.Markup.CustomXmlPartCollection sınıfını keşfedin.
type: docs
weight: 4620
url: /tr/net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

Özel XML Parçaları koleksiyonunu temsil eder. Öğeler[`CustomXmlPart`](../customxmlpart/) nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

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
| [Count](../../aspose.words.markup/customxmlpartcollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.markup/customxmlpartcollection/item/) { get; set; } | Belirtilen dizindeki bir öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add_1)(*[CustomXmlPart](../customxmlpart/)*) | Koleksiyona bir öğe ekler. |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add)(*string, string*) | Belirtilen XML ile yeni bir XML parçası oluşturur ve bunu koleksiyona ekler. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone/)() | Bu koleksiyonun ve öğelerinin derin bir kopyasını oluşturur. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid/)(*string*) | Tanımlayıcısına göre özel bir XML parçasını bulur ve döndürür. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat/)(*int*) | Belirtilen dizindeki bir öğeyi kaldırır. |

## Notlar

Normalde bu sınıfın örneklerini oluşturmanız gerekmez. Bir belgede depolanan özel XML data 'ye şu şekilde erişebilirsiniz:[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) mülk.

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

* class [CustomXmlPart](../customxmlpart/)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
