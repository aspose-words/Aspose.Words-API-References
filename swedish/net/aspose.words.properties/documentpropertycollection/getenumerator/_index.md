---
title: DocumentPropertyCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: DocumentPropertyCollection GetEnumerator metod. Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.properties/documentpropertycollection/getenumerator/
---
## DocumentPropertyCollection.GetEnumerator method

Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen.

```csharp
public IEnumerator<DocumentProperty> GetEnumerator()
```

## Exempel

Visar hur man arbetar med ett dokuments anpassade egenskaper.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Anpassade dokumentegenskaper är nyckel-värdepar som vi kan lägga till i dokumentet.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Samlingen sorterar de anpassade egenskaperna i alfabetisk ordning.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Skriv ut alla anpassade egenskaper i dokumentet.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Visa värdet för en anpassad egenskap med ett DOCPROPERTY-fält.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Vi kan hitta dessa anpassade egenskaper i Microsoft Word via "File" -> "Egenskaper" > "Avancerade egenskaper" > "Beställnings".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Nedan finns tre sätt att ta bort anpassade egenskaper från ett dokument.
// 1 - Ta bort efter index:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Ta bort efter namn:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Töm hela samlingen på en gång:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Se även

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
