---
title: CustomPartCollection.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: CustomPartCollection Ekleme yöntemiyle projenizi zahmetsizce geliştirin; sorunsuz entegrasyon ve verimlilik için koleksiyonunuza hızla öğeler ekleyin.
type: docs
weight: 40
url: /tr/net/aspose.words.markup/custompartcollection/add/
---
## CustomPartCollection.Add method

Koleksiyona bir öğe ekler.

```csharp
public void Add(CustomPart part)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| part | CustomPart | Eklenecek öğe. |

## Örnekler

Bir belgenin keyfi özel parça koleksiyonuna nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// İkinci parçayı klonla, ardından klonu koleksiyona ekle.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Koleksiyon üzerinde numaralandır ve her parçayı yazdır.
using (IEnumerator<CustomPart> enumerator = doc.PackageCustomParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Part index {index}:");
        Console.WriteLine($"\tName:\t\t\t\t{enumerator.Current.Name}");
        Console.WriteLine($"\tContent type:\t\t{enumerator.Current.ContentType}");
        Console.WriteLine($"\tRelationship type:\t{enumerator.Current.RelationshipType}");
        Console.WriteLine(enumerator.Current.IsExternal ?
            "\tSourced from outside the document" :
            $"\tStored within the document, length: {enumerator.Current.Data.Length} bytes");
        index++;
    }
}

// Bu koleksiyondan öğeleri tek tek veya hepsini birden kaldırabiliriz.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Ayrıca bakınız

* class [CustomPart](../../custompart/)
* class [CustomPartCollection](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
