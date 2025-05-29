---
title: BuiltInDocumentProperties.HeadingPairs
linktitle: HeadingPairs
articleTitle: HeadingPairs
second_title: .NET için Aspose.Words
description: Belge başlıklarını kolayca yönetmek ve belge organizasyonunuzu geliştirmek için BuiltInDocumentProperties'deki HeadingPairs özelliğini keşfedin.
type: docs
weight: 110
url: /tr/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

Belge başlıklarını ve adlarını belirtir.

```csharp
public object[] HeadingPairs { get; set; }
```

## Notlar

Bu dizide her başlık çifti iki eleman kaplar.

Çiftin ilk unsuru birString ve başlık adını belirtir. Çiftin ikinci öğesi birInt32 ve bu başlık için document parçalarının sayısını belirtir[`TitlesOfParts`](../titlesofparts/) mülk.

Bu özellikteki tüm başlık çiftleri için toplam sayım, öğenin sayısına eşit olmalıdır.[`TitlesOfParts`](../titlesofparts/) mülk.

Aspose.Words bu özelliği güncellemez.

## Örnekler

"HeadingPairs" ve "TitlesOfParts" özellikleri arasındaki ilişkiyi gösterir.

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Bu koleksiyonların birleşik değerlerini şu şekilde bulabiliriz:
// "Dosya" -> "Özellikler" -> "Gelişmiş Özellikler" -> "İçerikler" sekmesi.
// HeadingPairs özelliği, <string, int> çiftlerinin bir koleksiyonudur
// Bir başlığın kaç belge parçasına yayılacağını belirler.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// TitlesOfParts özelliği yukarıdaki başlıklara ait parçaların adlarını içerir.
string[] titlesOfParts = doc.BuiltInDocumentProperties.TitlesOfParts;

int headingPairsIndex = 0;
int titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs.Length)
{
    Console.WriteLine($"Parts for {headingPairs[headingPairsIndex++]}:");
    int partsCount = Convert.ToInt32(headingPairs[headingPairsIndex++]);

    for (int i = 0; i < partsCount; i++)
        Console.WriteLine($"\t\"{titlesOfParts[titlesOfPartsIndex++]}\"");
}
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
