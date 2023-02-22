---
title: Class CustomPart
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Markup.CustomPart sınıf. ISO/IEC 29500 standardı tarafından tanımlanmayan özel keyfi içerik bir bölümü temsil eder.
type: docs
weight: 3660
url: /tr/net/aspose.words.markup/custompart/
---
## CustomPart class

ISO/IEC 29500 standardı tarafından tanımlanmayan özel (keyfi içerik) bir bölümü temsil eder.

```csharp
public class CustomPart
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CustomPart](custompart/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ContentType](../../aspose.words.markup/custompart/contenttype/) { get; set; } | Bu özel parçanın içerik türünü belirtir. |
| [Data](../../aspose.words.markup/custompart/data/) { get; set; } | Bu özel parçanın verilerini içerir. |
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | `Yanlış` bu özel parça OOXML paketinin içinde saklanıyorsa.`Doğru` bu özel parça harici bir hedefse. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | OOXML paketi veya hedef URL içindeki bu parçanın mutlak adını alır veya ayarlar. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Üst parçadan bu özel parçaya olan ilişki türünü alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Nesnenin "yeterince derin" bir kopyasını oluşturur. [`Data`](./data/) değer. |

### Notlar

Bu sınıf, "bilinmeyen bir ilişkinin" hedefi olan bir OOXML parçasını temsil eder. ISO/IEC 29500'de tanımlanmayan tüm ilişkiler, "bilinmeyen ilişkiler" olarak kabul edilir. uyumlu olmaları koşuluyla, bir Office Açık XML belgesinde bilinmeyen ilişkilere izin verilir. ilişki işaretleme yönergelerine.

Microsoft Word, açma/kaydetme döngüleri sırasında özel parçaları korur. Bazı ek bilgiler burada bulunabilir: http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words ayrıca özel parçaların gidiş dönüşünü de yapar ve buna ek olarak, bu tür parçalara aracılığıyla programlı olarak erişmeye izin verir.`CustomPart` ve[`CustomPartCollection`](../custompartcollection/) nesneler.

Özel parçaları Özel XML Verileri ile karıştırmayın. Kullanmak[`CustomXmlPart`](../customxmlpart/) Özel XML Verilerine erişmek için 'ye ihtiyacınız varsa.

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

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)


