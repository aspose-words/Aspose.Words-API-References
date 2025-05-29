---
title: CustomXmlPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till specifika egenskaper med CustomXmlPropertyCollection. Hämta objekt efter namn för effektiv datahantering och förbättrad produktivitet.
type: docs
weight: 20
url: /sv/net/aspose.words.markup/customxmlpropertycollection/item/
---
## CustomXmlPropertyCollection indexer (1 of 2)

Hämtar en egenskap med det angivna namnet.

```csharp
public CustomXmlProperty this[string name] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| name | Skiftlägeskänsligt namn på egenskapen som ska hittas. |

## Exempel

Visar hur man arbetar med egenskaper för smarta taggar för att få djupgående information om smarta taggar.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// En smart tagg visas i ett dokument där Microsoft Word känner igen en del av texten som någon form av data,
// såsom ett namn, datum eller adress, och konverterar den till en hyperlänk som visar en lila prickad understrykning.
// I Word 2003 kan vi aktivera smarta taggar via "Verktyg" -> "Alternativ för autokorrigering..." -> "Smarta taggar".
// I vårt indatadokument finns tre objekt som Microsoft Word registrerat som smarta taggar.
// Smarta taggar kan vara kapslade, så den här samlingen innehåller fler.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// Medlemmen "Egenskaper" i en smarttagg innehåller dess metadata, som kommer att vara olika för varje typ av smarttagg.
// Egenskaperna för en smarttagg av typen "datum" innehåller dess år, månad och dag.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// Vi kan också komma åt egenskaperna på olika sätt, till exempel med ett nyckel-värde-par.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Nedan följer tre sätt att ta bort element från egenskapssamlingen.
// 1 - Ta bort via index:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - Ta bort efter namn:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - Rensa hela samlingen på en gång:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Se även

* class [CustomXmlProperty](../../customxmlproperty/)
* class [CustomXmlPropertyCollection](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)

---

## CustomXmlPropertyCollection indexer (2 of 2)

Hämtar en egenskap vid det angivna indexet.

```csharp
public CustomXmlProperty this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Nollbaserat index för egenskapen. |

## Exempel

Visar hur man arbetar med egenskaper för smarta taggar för att få djupgående information om smarta taggar.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// En smart tagg visas i ett dokument där Microsoft Word känner igen en del av texten som någon form av data,
// såsom ett namn, datum eller adress, och konverterar den till en hyperlänk som visar en lila prickad understrykning.
// I Word 2003 kan vi aktivera smarta taggar via "Verktyg" -> "Alternativ för autokorrigering..." -> "Smarta taggar".
// I vårt indatadokument finns tre objekt som Microsoft Word registrerat som smarta taggar.
// Smarta taggar kan vara kapslade, så den här samlingen innehåller fler.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// Medlemmen "Egenskaper" i en smarttagg innehåller dess metadata, som kommer att vara olika för varje typ av smarttagg.
// Egenskaperna för en smarttagg av typen "datum" innehåller dess år, månad och dag.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// Vi kan också komma åt egenskaperna på olika sätt, till exempel med ett nyckel-värde-par.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Nedan följer tre sätt att ta bort element från egenskapssamlingen.
// 1 - Ta bort via index:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - Ta bort efter namn:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - Rensa hela samlingen på en gång:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Se även

* class [CustomXmlProperty](../../customxmlproperty/)
* class [CustomXmlPropertyCollection](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
