---
title: Class CustomPartCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Markup.CustomPartCollection sınıf. Bir koleksiyonu temsil ederCustomPart nesneler.
type: docs
weight: 3670
url: /tr/net/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class

Bir koleksiyonu temsil eder[`CustomPart`](../custompart/) nesneler.

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
| [Count](../../aspose.words.markup/custompartcollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.markup/custompartcollection/item/) { get; set; } | Belirtilen dizindeki bir öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.markup/custompartcollection/add/)(CustomPart) | Koleksiyona bir öğe ekler. |
| [Clear](../../aspose.words.markup/custompartcollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Clone](../../aspose.words.markup/custompartcollection/clone/)() | Bu koleksiyonun ve öğelerinin derin bir kopyasını oluşturur. |
| [GetEnumerator](../../aspose.words.markup/custompartcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir Numaralandırıcı nesnesi döndürür. |
| [RemoveAt](../../aspose.words.markup/custompartcollection/removeat/)(int) | Belirtilen dizindeki bir öğeyi kaldırır. |

### Notlar

Normalde bu sınıfın örneklerini oluşturmanız gerekmez. OOXML paketiyle ilgili özel parçalara şu adresten erişirsiniz:[`PackageCustomParts`](../../aspose.words/document/packagecustomparts/) Emlak.

### Örnekler

Bir belgenin isteğe bağlı özel parça koleksiyonuna nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// İkinci bölümü klonlayın, ardından klonu koleksiyona ekleyin.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Koleksiyon üzerinde numaralandırın ve her parçayı yazdırın.
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

// Bu koleksiyondaki öğeleri tek tek veya bir kerede kaldırabiliriz.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Ayrıca bakınız

* class [CustomPart](../custompart/)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)


