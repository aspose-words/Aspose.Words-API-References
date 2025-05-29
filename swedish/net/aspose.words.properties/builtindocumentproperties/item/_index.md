---
title: BuiltInDocumentProperties.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till DocumentProperty-objekt med egenskapen BuiltInDocumentProperties Item. Effektivisera din dokumenthantering idag!
type: docs
weight: 140
url: /sv/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Returnerar en[`DocumentProperty`](../../documentproperty/) objekt med egenskapens namn.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| name | Det skiftlägeskänsliga namnet på den egenskap som ska hämtas. |

## Anmärkningar

Strängnamnen för egenskaperna motsvarar namnen på de typed -egenskaper som är tillgängliga från[`BuiltInDocumentProperties`](../).

Om du begär en egenskap som inte finns i dokumentet, men egenskapens namn name känns igen som ett giltigt inbyggt namn, kommer ett nytt[`DocumentProperty`](../../documentproperty/) skapas, läggs till i samlingen och returneras. Den nyskapade egenskapen tilldelas ett standardvärde (tom sträng, noll,`falsk` eller DateTime.MinValue beroende på type för den inbyggda egenskapen).

Om du begär en egenskap som inte finns i dokumentet och namnet inte känns igen som ett inbyggt namn, en`null` returneras.

## Exempel

Visar hur man arbetar med anpassade dokumentegenskaper.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Varje dokument innehåller en samling anpassade egenskaper, vilka, liksom de inbyggda egenskaperna, är nyckel-värde-par.
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
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
