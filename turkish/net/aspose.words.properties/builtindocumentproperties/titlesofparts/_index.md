---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: .NET için Aspose.Words
description: BuiltInDocumentProperties'deki TitlesOfParts özelliğini keşfedin. Gelişmiş organizasyon için net, özelleştirilebilir parça adlarıyla belge bölümlerini kolayca yönetin.
type: docs
weight: 330
url: /tr/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

Dizideki her dize, belgedeki bir parçanın adını belirtir.

```csharp
public string[] TitlesOfParts { get; set; }
```

## Notlar

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
