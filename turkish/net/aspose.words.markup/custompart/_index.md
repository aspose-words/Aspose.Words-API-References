---
title: CustomPart Class
linktitle: CustomPart
articleTitle: CustomPart
second_title: .NET için Aspose.Words
description: Esnek içerik yönetimi için Aspose.Words.Markup.CustomPart sınıfını keşfedin. ISO/IEC 29500'ün ötesinde benzersiz, standart dışı parçalar kolayca oluşturun!
type: docs
weight: 4590
url: /tr/net/aspose.words.markup/custompart/
---
## CustomPart class

ISO/IEC 29500 standardında tanımlanmayan özel (keyfi içerik) bir parçayı temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

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
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | Bu özel parça OOXML paketinin içinde saklanıyorsa yanlıştır. Bu özel parça harici bir hedefse doğru. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Bu parçanın OOXML paketindeki veya hedef URL'deki mutlak adını alır veya ayarlar. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Üst parçadan bu özel parçaya olan ilişki türünü alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Nesnenin "yeterince derin" bir kopyasını oluşturur. Nesnenin baytlarını çoğaltmaz.[`Data`](./data/) değer. |

## Notlar

Bu sınıf, "bilinmeyen bir ilişkinin" hedefi olan bir OOXML parçasını temsil eder. ISO/IEC 29500 içinde tanımlanmamış tüm ilişkiler "bilinmeyen ilişkiler" olarak kabul edilir. İlişki işaretleme yönergelerine uymaları koşuluyla, Office Open XML belgesi içinde bilinmeyen ilişkilere izin verilir.

Microsoft Word, açık/kaydetme döngüleri sırasında özel parçaları korur. Bazı ek bilgiler burada bulunabilir http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words ayrıca özel parçaları da döndürür ve buna ek olarak, bu tür parçalara programlı olarak erişime izin verir.`CustomPart` Ve[`CustomPartCollection`](../custompartcollection/) nesneler.

Özel parçaları Özel XML Verileriyle karıştırmayın. Kullanın[`CustomXmlPart`](../customxmlpart/) Özel XML Verilerine erişmek için 'ye ihtiyacınız varsa.

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

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
