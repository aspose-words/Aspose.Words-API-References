---
title: SdtListItem Class
linktitle: SdtListItem
articleTitle: SdtListItem
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Markup.SdtListItem, die für die effiziente Verwaltung von Listenelementen in ComboBox- und DropDownList-strukturierten Dokumenten entwickelt wurde.
type: docs
weight: 4710
url: /de/net/aspose.words.markup/sdtlistitem/
---
## SdtListItem class

Dieses Element gibt ein einzelnes Listenelement innerhalb eines übergeordnetenComboBox oderDropDownList strukturiertes Dokument-Tag.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltssteuerung](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class SdtListItem
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [SdtListItem](sdtlistitem/#constructor)(*string*) | Initialisiert eine neue Instanz dieser Klasse. |
| [SdtListItem](sdtlistitem/#constructor_1)(*string, string*) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayText](../../aspose.words.markup/sdtlistitem/displaytext/) { get; } | Ruft den Text ab, der im Laufinhalt anstelle des[`Value`](./value/) Attributinhalte für dieses Listenelement. |
| [Value](../../aspose.words.markup/sdtlistitem/value/) { get; } | Ruft den Wert dieses Listenelements ab. |

## Beispiele

Zeigt, wie mit Dokument-Tags in Form von Dropdown-Listen gearbeitet wird.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Ein Dropdown-Listen-strukturiertes Dokument-Tag ist ein Formular, das dem Benutzer erlaubt,
// Wählen Sie eine Option aus einer Liste aus, indem Sie mit der linken Maustaste klicken und das Formular in Microsoft Word öffnen.
// Die Eigenschaft „ListItems“ enthält alle Listenelemente und jedes Listenelement ist ein „SdtListItem“.
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Füge drei weitere Listenelemente hinzu. Initialisiere diese Elemente mit einem anderen Konstruktor als das erste Element.
// um Zeichenfolgen anzuzeigen, die sich von ihren Werten unterscheiden.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// Die Dropdown-Liste zeigt das erste Element an. Weisen Sie dem „SelectedValue“ ein anderes Listenelement zu, um es anzuzeigen.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Durchlaufen Sie die Sammlung und drucken Sie jedes Element.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

    // Entfernen Sie das letzte Listenelement.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Da unser Dropdown-Steuerelement standardmäßig so eingestellt ist, dass das entfernte Element angezeigt wird, geben Sie ihm ein Element zur Anzeige, das vorhanden ist.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Verwenden Sie die Methode „Clear“, um die gesamte Dropdown-Elementsammlung auf einmal zu leeren.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Siehe auch

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
