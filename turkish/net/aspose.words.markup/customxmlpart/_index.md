---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words for .NET
description: Aspose.Words.Markup.CustomXmlPart sınıf. Özel XML Veri Depolama Bölümünü temsil eder bir paket içindeki özel XML verileri C#'da.
type: docs
weight: 3920
url: /tr/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Özel XML Veri Depolama Bölümünü temsil eder (bir paket içindeki özel XML verileri).

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokümantasyon makalesi.

```csharp
public class CustomXmlPart
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CustomXmlPart](customxmlpart/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | Bu Özel XML Veri Depolama Parçasının XML içeriğini alır veya ayarlar. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Döngüsel artıklık denetimi (CRC) sağlama toplamını belirtir.[`Data`](./data/) içerik. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Bir OOXML belgesi içindeki bu özel XML bölümünü tanımlayan dizeyi alır veya ayarlar. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Bu özel XML bölümüyle ilişkili XML şemaları kümesini belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Nesnenin "yeterince derin" bir kopyasını oluşturur. Baytları çoğaltmaz[`Data`](./data/) değer. |

## Notlar

Bir DOCX veya DOC belgesi bir veya daha fazla Özel XML Veri Depolama bölümü içerebilir. Aspose.Words korur ve , Özel XML Verilerini oluşturmanıza ve çıkarmanıza olanak tanır.[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) Toplamak.

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

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
