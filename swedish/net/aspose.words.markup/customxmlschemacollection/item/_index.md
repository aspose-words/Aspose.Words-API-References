---
title: CustomXmlSchemaCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Upptäck hur du enkelt hanterar CustomXmlSchemaCollection-objekt. Lär dig att hämta eller ange element efter index för effektiviserad XML-datahantering.
type: docs
weight: 20
url: /sv/net/aspose.words.markup/customxmlschemacollection/item/
---
## CustomXmlSchemaCollection indexer

Hämtar eller ställer in elementet vid det angivna indexet.

```csharp
public string this[int index] { get; set; }
```

## Exempel

Visar hur man arbetar med en XML-schemasamling.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Lägg till en XML-schemaassociation.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Klona den anpassade XML-delens XML-schemaassociationssamling,
// och lägg sedan till ett par nya scheman till klonen.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Räkna upp schemana och skriv ut varje element.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Nedan följer tre sätt att ta bort scheman från samlingen.
// 1 - Ta bort ett schema via index:
schemas.RemoveAt(2);

// 2 - Ta bort ett schema efter värde:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Använd metoden "Rensa" för att tömma samlingen på en gång.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Se även

* class [CustomXmlSchemaCollection](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
