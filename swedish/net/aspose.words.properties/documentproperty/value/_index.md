---
title: DocumentProperty.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words för .NET
description: Upptäck hur du effektivt hanterar DocumentProperty-värden – hämta eller uppdatera enkelt egenskapsvärden för förbättrad dokumentkontroll och produktivitet.
type: docs
weight: 50
url: /sv/net/aspose.words.properties/documentproperty/value/
---
## DocumentProperty.Value property

Hämtar eller ställer in värdet på egenskapen.

```csharp
public object Value { get; set; }
```

## Anmärkningar

Kan inte vara`null`.

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

* class [DocumentProperty](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
