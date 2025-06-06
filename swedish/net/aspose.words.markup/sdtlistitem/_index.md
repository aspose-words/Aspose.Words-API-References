---
title: SdtListItem Class
linktitle: SdtListItem
articleTitle: SdtListItem
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Markup.SdtListItem, utformad för effektiv hantering av listobjekt i strukturerade dokument med kombinationsboxar och dropdownlists.
type: docs
weight: 4710
url: /sv/net/aspose.words.markup/sdtlistitem/
---
## SdtListItem class

Detta element anger ett enda listobjekt inom en överordnadComboBox ellerDropDownList strukturerad dokumenttagg.

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class SdtListItem
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [SdtListItem](sdtlistitem/#constructor)(*string*) | Initierar en ny instans av den här klassen. |
| [SdtListItem](sdtlistitem/#constructor_1)(*string, string*) | Initierar en ny instans av den här klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayText](../../aspose.words.markup/sdtlistitem/displaytext/) { get; } | Hämtar texten som ska visas i körningsinnehållet istället för[`Value`](./value/) attributinnehåll för detta listobjekt. |
| [Value](../../aspose.words.markup/sdtlistitem/value/) { get; } | Hämtar värdet för detta listobjekt. |

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

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
