---
title: CustomPart.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: CustomPart Name mülk. Bu parçanın OOXML paketi veya hedef URL içindeki mutlak adını alır veya ayarlar C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.markup/custompart/name/
---
## CustomPart.Name property

Bu parçanın OOXML paketi veya hedef URL içindeki mutlak adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

## Notlar

İlişki hedefi dahili ise bu özellik paket içindeki mutlak parça adıdır. İlişki hedefi harici ise bu özellik hedef URL'dir.

Varsayılan değer boş bir dizedir. Geçerli bir değer boş olmayan bir dize olmalıdır.

## Örnekler

Bir belgenin rastgele özel parça koleksiyonuna nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// İkinci kısmı klonlayın, ardından klonu koleksiyona ekleyin.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Koleksiyonun üzerinde numaralandırın ve her parçayı yazdırın.
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

// Bu koleksiyondaki öğeleri tek tek veya hepsini birden kaldırabiliriz.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Ayrıca bakınız

* class [CustomPart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
