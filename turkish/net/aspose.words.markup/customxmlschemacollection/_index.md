---
title: CustomXmlSchemaCollection
second_title: Aspose.Words for .NET API Referansı
description: Özel bir XML bölümüyle ilişkilendirilmiş XML şemalarını temsil eden dizeler koleksiyonu.
type: docs
weight: 3720
url: /tr/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

Özel bir XML bölümüyle ilişkilendirilmiş XML şemalarını temsil eden dizeler koleksiyonu.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item) { get; set; } | Belirtilen dizindeki öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add)(string) | Koleksiyona bir öğe ekler. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone)() | Bu nesnenin derin bir klonunu oluşturur. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir Numaralandırıcı nesnesi döndürür. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof)(string) | Koleksiyonda belirtilen değerin sıfır tabanlı dizinini döndürür. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove)(string) | Belirtilen değeri koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat)(int) | Belirtilen dizindeki bir değeri kaldırır. |

### Notlar

Bu sınıfın örneklerini oluşturmazsınız. Özel bir XML part XML şemaları koleksiyonuna,[`Schemas`](../customxmlpart/schemas) Emlak.

### Örnekler

Bir XML şema koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Bir XML şeması ilişkilendirmesi ekleyin.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Özel XML bölümünün XML şeması ilişkilendirme koleksiyonunu klonlayın,
// ve sonra klona birkaç yeni şema ekleyin.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Şemaları numaralandırın ve her bir elemanı yazdırın.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Aşağıda, şemaları koleksiyondan kaldırmanın üç yolu bulunmaktadır.
// 1 - Dizine göre şemayı kaldırın:
schemas.RemoveAt(2);

// 2 - Değere göre bir şemayı kaldırın:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Koleksiyonu bir kerede boşaltmak için "Temizle" yöntemini kullanın.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
