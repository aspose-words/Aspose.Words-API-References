---
title: DocumentPropertyCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words för .NET
description: Rensa enkelt alla egenskaper från din DocumentPropertyCollection med vår Clear-metod. Effektivisera din datahantering idag!
type: docs
weight: 30
url: /sv/net/aspose.words.properties/documentpropertycollection/clear/
---
## DocumentPropertyCollection.Clear method

Tar bort alla egenskaper från samlingen.

```csharp
public void Clear()
```

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
