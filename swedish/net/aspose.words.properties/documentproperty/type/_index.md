---
title: DocumentProperty.Type
second_title: Aspose.Words för .NET API Referens
description: DocumentProperty fast egendom. Hämtar datatypen för egenskapen.
type: docs
weight: 40
url: /sv/net/aspose.words.properties/documentproperty/type/
---
## DocumentProperty.Type property

Hämtar datatypen för egenskapen.

```csharp
public PropertyType Type { get; }
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

* enum [PropertyType](../../propertytype/)
* class [DocumentProperty](../)
* namnutrymme [Aspose.Words.Properties](../../documentproperty/)
* hopsättning [Aspose.Words](../../../)


