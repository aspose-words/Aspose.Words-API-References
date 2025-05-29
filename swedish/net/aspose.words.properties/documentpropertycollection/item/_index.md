---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till DocumentProperty-objekt med vårt DocumentPropertyCollection-objekt. Hämta egenskaper efter namn för smidig dokumenthantering.
type: docs
weight: 20
url: /sv/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

Returnerar en[`DocumentProperty`](../../documentproperty/) objekt med egenskapens namn.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| name | Det skiftlägeskänsliga namnet på den egenskap som ska hämtas. |

## Anmärkningar

Returer`null` om en egenskap med det angivna namnet inte hittas.

## Exempel

Visar hur man skapar en anpassad dokumentegenskap som innehåller datum och tid.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

### Se även

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

Returnerar en[`DocumentProperty`](../../documentproperty/) objekt av index.

```csharp
public DocumentProperty this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Nollbaserat index för[`DocumentProperty`](../../documentproperty/) att hämta. |

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
* class [DocumentPropertyCollection](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
