---
title: SdtListItemCollection Class
linktitle: SdtListItemCollection
articleTitle: SdtListItemCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.Markup.SdtListItemCollection klas. Bietet Zugriff aufSdtListItem Elemente eines strukturierten DokumentTags in C#.
type: docs
weight: 4030
url: /de/net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

Bietet Zugriff auf[`SdtListItem`](../sdtlistitem/) Elemente eines strukturierten Dokument-Tags.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltskontrolle](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | Ruft die Anzahl der Elemente in der Sammlung ab. |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | Gibt a zurück[`SdtListItem`](../sdtlistitem/) Objekt erhält seinen nullbasierten Index in der Sammlung. |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | Gibt den aktuell ausgewählten Wert in dieser Liste an. Nullwert zulässig, was bedeutet, dass kein aktuell ausgewählter Eintrag mit dieser Listenelementsammlung verknüpft ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(*[SdtListItem](../sdtlistitem/)*) | Fügt ein Element zu dieser Sammlung hinzu. |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | Löscht alle Elemente aus dieser Sammlung. |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, das zum Durchlaufen aller Elemente in der Sammlung verwendet werden kann. |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(*int*) | Entfernt ein Listenelement am angegebenen Index. |

## Beispiele

Zeigt, wie mit strukturierten Dropdown-Dokument-Tags gearbeitet wird.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Ein strukturiertes Dokument-Tag mit Dropdown-Liste ist ein Formular, das es dem Benutzer ermöglicht
// Wählen Sie eine Option aus einer Liste aus, indem Sie mit der linken Maustaste klicken und das Formular in Microsoft Word öffnen.
// Die Eigenschaft „ListItems“ enthält alle Listenelemente und jedes Listenelement ist ein „SdtListItem“.
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// 3 weitere Listenelemente hinzufügen. Initialisieren Sie diese Elemente mit einem anderen Konstruktor als dem ersten Element
// um Zeichenfolgen anzuzeigen, die sich von ihren Werten unterscheiden.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// Die Dropdown-Liste zeigt das erste Element an. Weisen Sie dem „SelectedValue“ ein anderes Listenelement zu, um es anzuzeigen.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Die Sammlung aufzählen und jedes Element drucken.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Letztes Listenelement entfernen.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Da unser Dropdown-Steuerelement standardmäßig so eingestellt ist, dass es das entfernte Element anzeigt, geben Sie ihm ein anzuzeigendes Element, das vorhanden ist.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Verwenden Sie die Methode „Clear“, um die gesamte Dropdown-Elementsammlung auf einmal zu leeren.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Siehe auch

* class [SdtListItem](../sdtlistitem/)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
