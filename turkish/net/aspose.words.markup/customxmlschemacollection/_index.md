---
title: Class CustomXmlSchemaCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Markup.CustomXmlSchemaCollection sınıf. Özel bir XML bölümüyle ilişkili XML şemalarını temsil eden dizelerden oluşan bir koleksiyon.
type: docs
weight: 3960
url: /tr/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

Özel bir XML bölümüyle ilişkili XML şemalarını temsil eden dizelerden oluşan bir koleksiyon.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokümantasyon makalesi.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | Koleksiyonda yer alan öğelerin sayısını alır. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | Belirtilen dizindeki öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(string) | Koleksiyona bir öğe ekler. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | Bu nesnenin derin bir klonunu oluşturur. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(string) | Koleksiyonda belirtilen değerin sıfır tabanlı dizinini döndürür. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(string) | Belirtilen değeri koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(int) | Belirtilen dizindeki bir değeri kaldırır. |

### Notlar

Bu sınıfın örneklerini oluşturmazsınız. Özel bir XML part 'nin XML şemaları koleksiyonuna şu yolla erişebilirsiniz:[`Schemas`](../customxmlpart/schemas/) mülk.

### Örnekler

XML şeması koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Bir XML şeması ilişkisi ekleyin.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Özel XML bölümünün XML şeması ilişkilendirme koleksiyonunu kopyalayın,
// ve ardından klona birkaç yeni şema ekleyin.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Şemaları numaralandırın ve her öğeyi yazdırın.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Aşağıda şemaları koleksiyondan kaldırmanın üç yolu verilmiştir.
// 1 - Bir şemayı dizine göre kaldırın:
schemas.RemoveAt(2);

// 2 - Bir şemayı değere göre kaldırın:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Koleksiyonu bir kerede boşaltmak için "Temizle" yöntemini kullanın.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)


