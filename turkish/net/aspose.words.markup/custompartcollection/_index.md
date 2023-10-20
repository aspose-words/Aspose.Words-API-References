---
title: CustomPartCollection Class
linktitle: CustomPartCollection
articleTitle: CustomPartCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Markup.CustomPartCollection sınıf. Aşağıdakilerin bir koleksiyonunu temsil ederCustomPart nesneler C#'da.
type: docs
weight: 3910
url: /tr/net/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class

Aşağıdakilerin bir koleksiyonunu temsil eder:[`CustomPart`](../custompart/) nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokümantasyon makalesi.

```csharp
public class CustomPartCollection : IEnumerable<CustomPart>
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CustomPartCollection](custompartcollection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.markup/custompartcollection/count/) { get; } | Koleksiyonda yer alan öğelerin sayısını alır. |
| [Item](../../aspose.words.markup/custompartcollection/item/) { get; set; } | Belirtilen dizindeki bir öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.markup/custompartcollection/add/)(*[CustomPart](../custompart/)*) | Koleksiyona bir öğe ekler. |
| [Clear](../../aspose.words.markup/custompartcollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Clone](../../aspose.words.markup/custompartcollection/clone/)() | Bu koleksiyonun ve içindeki öğelerin derin bir kopyasını oluşturur. |
| [GetEnumerator](../../aspose.words.markup/custompartcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |
| [RemoveAt](../../aspose.words.markup/custompartcollection/removeat/)(*int*) | Belirtilen dizindeki bir öğeyi kaldırır. |

## Notlar

Normalde bu sınıfın örneklerini oluşturmanıza gerek yoktur. OOXML paketiyle ilgili özel bölümlerine şu adresten erişebilirsiniz:[`PackageCustomParts`](../../aspose.words/document/packagecustomparts/) mülk.

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

* class [CustomPart](../custompart/)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
