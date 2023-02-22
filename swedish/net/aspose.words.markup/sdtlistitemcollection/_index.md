---
title: Class SdtListItemCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Markup.SdtListItemCollection klass. Ger tillgång tillSdtListItemelement i en strukturerad dokumenttagg.
type: docs
weight: 3790
url: /sv/net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

Ger tillgång till[`SdtListItem`](../sdtlistitem/)element i en strukturerad dokumenttagg.

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | Får antal föremål i samlingen. |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | Returnerar en[`SdtListItem`](../sdtlistitem/) objekt med tanke på dess nollbaserade index i samlingen. |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | Anger för närvarande valt värde i denna lista. Nullvärde tillåtet, vilket betyder att ingen för närvarande vald post är associerad med denna listobjektsamling. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(SdtListItem) | Lägger till ett föremål i den här samlingen. |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | Rensar alla objekt från den här samlingen. |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(int) | Tar bort ett listobjekt vid det angivna indexet. |

### Exempel

Visar hur man arbetar med strukturerade dokumenttaggar i listrutan.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// En rullgardinslista med strukturerad dokumenttagg är ett formulär som låter användaren
// välj ett alternativ från en lista genom att vänsterklicka och öppna formuläret i Microsoft Word.
// Egenskapen "ListItems" innehåller alla listobjekt, och varje listobjekt är en "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Lägg till ytterligare 3 listobjekt. Initiera dessa objekt med en annan konstruktor än det första objektet
// för att visa strängar som skiljer sig från deras värden.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// Rullgardinslistan visar det första objektet. Tilldela ett annat listobjekt till "SelectedValue" för att visa det.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Räkna upp över samlingen och skriv ut varje element.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

  // Ta bort det sista listobjektet.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Eftersom vår rullgardinskontroll är inställd på att visa det borttagna objektet som standard, ge det ett objekt att visa som finns.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Använd "Rensa"-metoden för att tömma hela rullgardinsmenyn på en gång.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Se även

* class [SdtListItem](../sdtlistitem/)
* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)


