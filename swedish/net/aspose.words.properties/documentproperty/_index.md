---
title: DocumentProperty Class
linktitle: DocumentProperty
articleTitle: DocumentProperty
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Properties.DocumentProperty för att effektivt hantera anpassade och inbyggda dokumentegenskaper. Förbättra din dokumenthantering idag!
type: docs
weight: 5200
url: /sv/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

Representerar en anpassad eller inbyggd dokumentegenskap.

För att lära dig mer, besök[Arbeta med dokumentegenskaper](https://docs.aspose.com/words/net/work-with-document-properties/) dokumentationsartikel.

```csharp
public class DocumentProperty
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | Visar om den här egenskapen är länkad till innehåll eller inte. |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | Hämtar källan för en länkad anpassad dokumentegenskap. |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | Returnerar namnet på egenskapen. |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | Hämtar datatypen för egenskapen. |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | Hämtar eller ställer in värdet på egenskapen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | Returnerar egenskapsvärdet som bool. |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | Returnerar egenskapsvärdet som en byte-array. |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | Returnerar egenskapsvärdet som**Datum och tid** i UTC. |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | Returnerar egenskapsvärdet som double. |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | Returnerar egenskapsvärdet som ett heltal. |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | Returnerar egenskapsvärdet som en sträng formaterad enligt aktuell språkinställning. |

## Exempel

Visar hur man arbetar med inbyggda dokumentegenskaper.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Objektet "Dokument" innehåller en del av dess metadata i sina medlemmar.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Dokumentet lagrar även metadata i sina inbyggda egenskaper.
// Varje inbyggd egenskap är en medlem av dokumentets "BuiltInDocumentProperties"-objekt.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Vissa egenskaper kan lagra flera värden.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

### Se även

* class [DocumentPropertyCollection](../documentpropertycollection/)
* namnutrymme [Aspose.Words.Properties](../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../)
