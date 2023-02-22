---
title: Document.BuiltInDocumentProperties
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Returnerar en samling som representerar alla inbyggda dokumentegenskaper i dokumentet.
type: docs
weight: 40
url: /sv/net/aspose.words/document/builtindocumentproperties/
---
## Document.BuiltInDocumentProperties property

Returnerar en samling som representerar alla inbyggda dokumentegenskaper i dokumentet.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

### Exempel

Visar hur man arbetar med inbyggda dokumentegenskaper.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// "Dokument"-objektet innehåller en del av dess metadata i sina medlemmar.
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

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


