---
title: Class CustomPart
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Markup.CustomPart sınıf. ISO/IEC 29500 standardı tarafından tanımlanmayan özel rastgele içerik bir parçayı temsil eder.
type: docs
weight: 3900
url: /tr/net/aspose.words.markup/custompart/
---
## CustomPart class

ISO/IEC 29500 standardı tarafından tanımlanmayan özel (rastgele içerik) bir parçayı temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokümantasyon makalesi.

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
| [ContentType](../../aspose.words.markup/custompart/contenttype/) { get; set; } | Bu özel bölümün içerik türünü belirtir. |
| [Data](../../aspose.words.markup/custompart/data/) { get; set; } | Bu özel parçanın verilerini içerir. |
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | Bu özel parça OOXML paketinin içinde saklanıyorsa yanlış. Bu özel parça harici bir hedefse doğrudur. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Bu parçanın OOXML paketi veya hedef URL içindeki mutlak adını alır veya ayarlar. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Üst parçadan bu özel parçaya ilişkin ilişki türünü alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Nesnenin "yeterince derin" bir kopyasını oluşturur. Baytları çoğaltmaz[`Data`](./data/) değer. |

### Notlar

Bu sınıf, "bilinmeyen bir ilişkinin" hedefi olan bir OOXML parçasını temsil eder. ISO/IEC 29500'de tanımlanmayan tüm ilişkiler, "bilinmeyen ilişkiler" olarak kabul edilir. Bir Office Açık XML belgesinde, uyumlu olmaları koşuluyla, bilinmeyen ilişkilere izin verilir. ilişki işaretleme yönergelerine.

Microsoft Word, açma/kaydetme döngüleri sırasında özel parçaları korur. Bazı ek bilgileri burada bulabilirsiniz http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words ayrıca özel parçalara gidiş dönüş sağlar ve ayrıca bu tür parçalara programlı olarak erişime izin verir.`CustomPart` Ve[`CustomPartCollection`](../custompartcollection/) nesneler.

Özel parçaları Özel XML Verileriyle karıştırmayın. Kullanmak[`CustomXmlPart`](../customxmlpart/) Özel XML Verilerine erişmek için 'ye ihtiyacınız varsa.

### Örnekler

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

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)


