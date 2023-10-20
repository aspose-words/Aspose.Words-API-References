---
title: CustomXmlPropertyCollection Class
linktitle: CustomXmlPropertyCollection
articleTitle: CustomXmlPropertyCollection
second_title: Aspose.Words för .NET
description: Aspose.Words.Markup.CustomXmlPropertyCollection klass. Representerar en samling anpassade XMLattribut eller egenskaper för smarta taggar i C#.
type: docs
weight: 3950
url: /sv/net/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class

Representerar en samling anpassade XML-attribut eller egenskaper för smarta taggar.

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class CustomXmlPropertyCollection : IEnumerable<CustomXmlProperty>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpropertycollection/count/) { get; } | Hämtar antalet element som finns i samlingen. |
| [Item](../../aspose.words.markup/customxmlpropertycollection/item/) { get; } | Får en egenskap med det angivna namnet. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpropertycollection/add/)(*[CustomXmlProperty](../customxmlproperty/)*) | Lägger till en egenskap i samlingen. |
| [Clear](../../aspose.words.markup/customxmlpropertycollection/clear/)() | Tar bort alla element från samlingen. |
| [Contains](../../aspose.words.markup/customxmlpropertycollection/contains/)(*string*) | Bestämmer om samlingen innehåller en egenskap med det angivna namnet. |
| [GetEnumerator](../../aspose.words.markup/customxmlpropertycollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [IndexOfKey](../../aspose.words.markup/customxmlpropertycollection/indexofkey/)(*string*) | Returnerar det nollbaserade indexet för den angivna egenskapen i samlingen. |
| [Remove](../../aspose.words.markup/customxmlpropertycollection/remove/)(*string*) | Tar bort en egenskap med det angivna namnet från samlingen. |
| [RemoveAt](../../aspose.words.markup/customxmlpropertycollection/removeat/)(*int*) | Tar bort en egenskap vid det angivna indexet. |

## Anmärkningar

Objekt är[`CustomXmlProperty`](../customxmlproperty/) föremål.

## Exempel

Visar hur man arbetar med smarta taggars egenskaper för att få djupgående information om smarta taggar.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// En smart tagg visas i ett dokument med Microsoft Word känner igen en del av sin text som någon form av data,
// som ett namn, datum eller adress, och konverterar det till en hyperlänk som visar en lila prickad underlinje.
// I Word 2003 kan vi aktivera smarta taggar via "Verktyg" -> "Autokorrigeringsalternativ..." -> "SmartTags".
// I vårt indatadokument finns det tre objekt som Microsoft Word registrerade som smarta taggar.
// Smarta taggar kan vara kapslade, så den här samlingen innehåller fler.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// "Properties"-medlemmen i en smart tagg innehåller dess metadata, som kommer att vara olika för varje typ av smart tagg.
// Egenskaperna för en smart tagg av "datum"-typ innehåller dess år, månad och dag.
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

// Vi kan också komma åt egenskaperna på olika sätt, till exempel ett nyckel-värdepar.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Nedan finns tre sätt att ta bort element från egenskapssamlingen.
// 1 - Ta bort efter index:
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

* class [CustomXmlProperty](../customxmlproperty/)
* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
