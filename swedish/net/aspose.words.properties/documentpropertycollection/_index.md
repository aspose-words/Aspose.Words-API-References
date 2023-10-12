---
title: Class DocumentPropertyCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Properties.DocumentPropertyCollection klass. Basklass förBuiltInDocumentProperties ochCustomDocumentProperties samlingar.
type: docs
weight: 4480
url: /sv/net/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class

Basklass för[`BuiltInDocumentProperties`](../builtindocumentproperties/) och[`CustomDocumentProperties`](../customdocumentproperties/) samlingar.

För att lära dig mer, besök[Arbeta med dokumentegenskaper](https://docs.aspose.com/words/net/work-with-document-properties/) dokumentationsartikel.

```csharp
public abstract class DocumentPropertyCollection : IEnumerable<DocumentProperty>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Får antal föremål i samlingen. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Returnerar en[`DocumentProperty`](../documentproperty/) objekt efter index. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Returnerar en[`DocumentProperty`](../documentproperty/) objekt efter egenskapens namn. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Tar bort alla egenskaper från samlingen. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(string) | Returnerar`Sann` om en egenskap med det angivna namnet finns i samlingen. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(string) | Hämtar indexet för en egenskap efter namn. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(string) | Tar bort en egenskap med det angivna namnet från samlingen. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(int) | Tar bort en egenskap vid det angivna indexet. |

### Anmärkningar

Namnen på egenskaperna är skiftlägesokänsliga.

Fastigheterna i samlingen är sorterade alfabetiskt efter namn.

### Exempel

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

* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)
* class [DocumentProperty](../documentproperty/)
* namnutrymme [Aspose.Words.Properties](../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../)


