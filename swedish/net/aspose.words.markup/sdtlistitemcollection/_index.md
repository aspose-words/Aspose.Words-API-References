---
title: SdtListItemCollection Class
linktitle: SdtListItemCollection
articleTitle: SdtListItemCollection
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.Markup.SdtListItemCollection för smidig åtkomst till SdtListItem-element och förbättra strukturerad dokumenthantering utan ansträngning.
type: docs
weight: 4720
url: /sv/net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

Ger åtkomst till[`SdtListItem`](../sdtlistitem/) element i en strukturerad dokumenttagg.

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | Hämtar antalet objekt i samlingen. |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | Returnerar en[`SdtListItem`](../sdtlistitem/) objekt givet dess nollbaserade index i samlingen. |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | Anger det valda värdet i den här listan. Nullvärde tillåtet, vilket innebär att ingen vald post är associerad med den här listobjektsamlingen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(*[SdtListItem](../sdtlistitem/)*) | Lägger till ett objekt i den här samlingen. |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | Rensar alla objekt från den här samlingen. |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | Returnerar ett uppräknarobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(*int*) | Tar bort ett listobjekt vid det angivna indexet. |

## Exempel

Visar hur man arbetar med strukturerade dokumenttaggar i en nedrullningsbar listruta.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// En tagg för strukturerat dokument med en nedrullningsbar lista är ett formulär som låter användaren
// välj ett alternativ från en lista genom att vänsterklicka och öppna formuläret i Microsoft Word.
// Egenskapen "ListItems" innehåller alla listobjekt, och varje listobjekt är ett "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Lägg till 3 listobjekt till. Initiera dessa objekt med en annan konstruktor än det första objektet
// för att visa strängar som skiljer sig från deras värden.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// Listrutan visar det första objektet. Tilldela ett annat listobjekt till "SelectedValue" för att visa det.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Räkna upp samlingen och skriv ut varje element.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Ta bort det sista listobjektet.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Eftersom vår rullgardinsmeny är inställd på att visa det borttagna objektet som standard, ge det ett objekt att visa som finns.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Använd metoden "Rensa" för att tömma hela listrutan med objekt på en gång.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Se även

* class [SdtListItem](../sdtlistitem/)
* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
