---
title: CustomXmlSchemaCollection.Clone
linktitle: Clone
articleTitle: Clone
second_title: .NET için Aspose.Words
description: Kusursuz bir derin kopyalama deneyimi için CustomXmlSchemaCollection'ınızı Clone yöntemimizle zahmetsizce çoğaltın. XML yönetiminizi bugün geliştirin!
type: docs
weight: 50
url: /tr/net/aspose.words.markup/customxmlschemacollection/clone/
---
## CustomXmlSchemaCollection.Clone method

Bu nesnenin derin bir klonunu oluşturur.

```csharp
public CustomXmlSchemaCollection Clone()
```

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

* class [CustomXmlSchemaCollection](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
