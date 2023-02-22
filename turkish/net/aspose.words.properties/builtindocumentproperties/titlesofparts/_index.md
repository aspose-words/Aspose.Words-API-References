---
title: BuiltInDocumentProperties.TitlesOfParts
second_title: Aspose.Words for .NET API Referansı
description: BuiltInDocumentProperties mülk. Dizideki her dize belgedeki bir parçanın adını belirtir.
type: docs
weight: 300
url: /tr/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

Dizideki her dize, belgedeki bir parçanın adını belirtir.

```csharp
public string[] TitlesOfParts { get; set; }
```

### Notlar

Aspose.Words bu özelliği güncellemez.

### Örnekler

"HeadingPairs" ve "TitlesOfParts" özellikleri arasındaki ilişkiyi gösterir.

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Bu koleksiyonların birleşik değerlerini şuradan bulabiliriz:
// "Dosya" -> "Özellikler" -> "Gelişmiş Özellikler" -> "İçindekiler" sekmesi.
// HeadingPairs özelliği, <string, int> çiftler ki
// bir başlığın kaç belge parçasına yayılacağını belirler.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// TitlesOfParts özelliği, yukarıdaki başlıklara ait olan parçaların isimlerini içerir.
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
* ad alanı [Aspose.Words.Properties](../../builtindocumentproperties/)
* toplantı [Aspose.Words](../../../)


