---
title: DocumentPropertyCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words för .NET
description: DocumentPropertyCollection Count fast egendom. Får antal föremål i samlingen i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.properties/documentpropertycollection/count/
---
## DocumentPropertyCollection.Count property

Får antal föremål i samlingen.

```csharp
public int Count { get; }
```

## Exempel

Visar hur man arbetar med anpassade dokumentegenskaper.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Varje dokument innehåller en samling anpassade egenskaper, som, liksom de inbyggda egenskaperna, är nyckel-värdepar.
 // Dokumentet har en fast lista med inbyggda egenskaper. Användaren skapar alla anpassade egenskaper.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Se även

* class [DocumentPropertyCollection](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
