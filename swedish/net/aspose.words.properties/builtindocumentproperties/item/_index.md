---
title: BuiltInDocumentProperties.Item
second_title: Aspose.Words för .NET API Referens
description: BuiltInDocumentProperties fast egendom. Returnerar enDocumentProperty objekt efter egenskapens namn.
type: docs
weight: 130
url: /sv/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Returnerar en[`DocumentProperty`](../../documentproperty/) objekt efter egenskapens namn.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| name | Det skiftlägesokänsliga namnet på egendomen som ska hämtas. |

### Anmärkningar

Strängnamnen på egenskaperna motsvarar namnen på de typd egenskaper som är tillgängliga från[`BuiltInDocumentProperties`](../).

Om du begär en egenskap som inte finns i dokumentet, men fastighetens namn erkänns som ett giltigt inbyggt namn, kommer en ny[`DocumentProperty`](../../documentproperty/) skapas, läggs till i samlingen och returneras. Den nyskapade egenskapen är tilldelad ett standardvärde (tom sträng, noll,`falsk` eller DateTime.MinValue beroende på typen för den inbyggda egenskapen).

Om du begär en egenskap som inte finns i dokumentet och namnet inte känns igen som ett inbyggt namn,`null` returneras.

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

* class [DocumentProperty](../../documentproperty/)
* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../builtindocumentproperties/)
* hopsättning [Aspose.Words](../../../)


