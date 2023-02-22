---
title: CustomXmlSchemaCollection.GetEnumerator
second_title: Aspose.Words for .NET API Referansı
description: CustomXmlSchemaCollection yöntem. Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir Numaralandırıcı nesnesi döndürür.
type: docs
weight: 60
url: /tr/net/aspose.words.markup/customxmlschemacollection/getenumerator/
---
## CustomXmlSchemaCollection.GetEnumerator method

Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir Numaralandırıcı nesnesi döndürür.

```csharp
public IEnumerator<string> GetEnumerator()
```

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

* class [CustomXmlSchemaCollection](../)
* ad alanı [Aspose.Words.Markup](../../customxmlschemacollection/)
* toplantı [Aspose.Words](../../../)


