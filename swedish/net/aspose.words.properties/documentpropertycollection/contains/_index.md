---
title: DocumentPropertyCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words för .NET
description: Upptäck om en egenskap finns i DocumentPropertyCollection med vår effektiva Contains-metod. Förenkla din datahantering idag!
type: docs
weight: 40
url: /sv/net/aspose.words.properties/documentpropertycollection/contains/
---
## DocumentPropertyCollection.Contains method

Returer`sann` om en egenskap med det angivna namnet finns i samlingen.

```csharp
public bool Contains(string name)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Egenskapens namn som inte är skiftlägeskänsligt. |

### Returvärde

`sann` om egendomen finns i samlingen;`falsk` annat.

## Exempel

Visar hur man arbetar med ett dokuments anpassade egenskaper.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Anpassade dokumentegenskaper är nyckel-värde-par som vi kan lägga till i dokumentet.
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

// Visa värdet för en anpassad egenskap med hjälp av ett DOCPROPERTY-fält.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Vi hittar dessa anpassade egenskaper i Microsoft Word via "Arkiv" -> "Egenskaper" > "Avancerade egenskaper" > "Anpassad".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Nedan följer tre sätt att ta bort anpassade egenskaper från ett dokument.
// 1 - Ta bort via index:
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

* class [DocumentPropertyCollection](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
