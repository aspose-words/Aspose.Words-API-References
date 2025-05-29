---
title: CustomXmlSchemaCollection Class
linktitle: CustomXmlSchemaCollection
articleTitle: CustomXmlSchemaCollection
second_title: .NET için Aspose.Words
description: Özel XML parçalarına bağlı XML şemalarını yönetmek, belge esnekliğini ve denetimini artırmak için Aspose.Words.Markup.CustomXmlSchemaCollection sınıfını keşfedin.
type: docs
weight: 4650
url: /tr/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

Özel bir XML parçasıyla ilişkili XML şemalarını temsil eden dizelerin bir koleksiyonu.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | Belirtilen dizindeki öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(*string*) | Koleksiyona bir öğe ekler. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | Bu nesnenin derin bir klonunu oluşturur. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(*string*) | Koleksiyondaki belirtilen değerin sıfır tabanlı dizinini döndürür. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(*string*) | Belirtilen değeri koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(*int*) | Belirtilen dizindeki bir değeri kaldırır. |

## Notlar

Bu sınıfın örneklerini oluşturmazsınız. Özel bir XML part 'nin XML şemaları koleksiyonuna şu şekilde erişirsiniz:[`Schemas`](../customxmlpart/schemas/) mülk.

## Örnekler

XML şema koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Bir XML şema ilişkisi ekleyin.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Özel XML parçasının XML şema ilişkilendirme koleksiyonunu kopyala,
// ve ardından klona birkaç yeni şema ekleyin.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-örneği");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Şemaları numaralandır ve her bir elemanı yazdır.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Aşağıda şemaları koleksiyondan kaldırmanın üç yolu bulunmaktadır.
// 1 - Dizin yoluyla bir şemayı kaldır:
schemas.RemoveAt(2);

// 2 - Bir şemayı değerine göre kaldır:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Koleksiyonu bir defada boşaltmak için "Clear" metodunu kullanın.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
