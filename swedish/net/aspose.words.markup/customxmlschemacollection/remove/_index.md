---
title: CustomXmlSchemaCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words för .NET
description: Hantera enkelt din CustomXmlSchemaCollection med metoden Remove för att eliminera specifika värden, vilket förbättrar dataorganisation och effektivitet.
type: docs
weight: 80
url: /sv/net/aspose.words.markup/customxmlschemacollection/remove/
---
## CustomXmlSchemaCollection.Remove method

Tar bort det angivna värdet från samlingen.

```csharp
public void Remove(string name)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Det skiftlägeskänsliga värdet som ska tas bort. |

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
