---
title: Class CustomDocumentProperties
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Properties.CustomDocumentProperties klass. En samling anpassade dokumentegenskaper.
type: docs
weight: 4460
url: /sv/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

En samling anpassade dokumentegenskaper.

För att lära dig mer, besök[Arbeta med dokumentegenskaper](https://docs.aspose.com/words/net/work-with-document-properties/) dokumentationsartikel.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
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
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(string, bool) | Skapar en ny anpassad dokumentegenskap förBoolean datatyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(string, DateTime) | Skapar en ny anpassad dokumentegenskap förDateTime datatyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(string, double) | Skapar en ny anpassad dokumentegenskap förDouble datatyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(string, int) | Skapar en ny anpassad dokumentegenskap förNumber datatyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(string, string) | Skapar en ny anpassad dokumentegenskap förString datatyp. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(string, string) | Skapar en ny länkad till innehåll anpassad dokumentegenskap. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Tar bort alla egenskaper från samlingen. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(string) | Returnerar`Sann` om en egenskap med det angivna namnet finns i samlingen. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(string) | Hämtar indexet för en egenskap efter namn. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(string) | Tar bort en egenskap med det angivna namnet från samlingen. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(int) | Tar bort en egenskap vid det angivna indexet. |

### Anmärkningar

Varje[`DocumentProperty`](../documentproperty/) objekt representerar en anpassad egenskap för ett containerdokument.

Namnen på egenskaperna är skiftlägesokänsliga.

Fastigheterna i samlingen är sorterade alfabetiskt efter namn.

### Exempel

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

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* namnutrymme [Aspose.Words.Properties](../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../)


