---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: .NET için Aspose.Words
description: Paketler içindeki özel XML veri depolamasının verimli yönetimi için Aspose.Words.Markup.CustomXmlPart sınıfını keşfedin. Belge işlemenizi bugün geliştirin!
type: docs
weight: 4610
url: /tr/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Özel XML Veri Depolama Parçasını (bir paket içindeki özel XML verileri) temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

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
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Döngüsel yedeklilik denetimi (CRC) toplamını belirtir[`Data`](./data/) içerik. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Bu özel XML parçasını bir OOXML belgesi içinde tanımlayan dizeyi alır veya ayarlar. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Bu özel XML parçasıyla ilişkili XML şemaları kümesini belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Nesnenin "yeterince derin" bir kopyasını oluşturur. Nesnenin baytlarını çoğaltmaz.[`Data`](./data/) değer. |

## Notlar

Bir DOCX veya DOC belgesi bir veya daha fazla Özel XML Veri Depolama parçası içerebilir. Aspose.Words korur ve Özel XML Verilerini oluşturmanıza ve çıkarmanıza olanak tanır[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) koleksiyon.

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

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
