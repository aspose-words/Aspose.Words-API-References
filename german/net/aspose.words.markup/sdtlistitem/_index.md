---
title: Class SdtListItem
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Markup.SdtListItem klas. Dieses Element gibt ein einzelnes Listenelement innerhalb eines übergeordneten Elements anComboBox oderDropDownList Strukturiertes DokumentTag.
type: docs
weight: 4020
url: /de/net/aspose.words.markup/sdtlistitem/
---
## SdtListItem class

Dieses Element gibt ein einzelnes Listenelement innerhalb eines übergeordneten Elements anComboBox oderDropDownList Strukturiertes Dokument-Tag.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltskontrolle](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class SdtListItem
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [SdtListItem](sdtlistitem/#constructor)(string) | Initialisiert eine neue Instanz dieser Klasse. |
| [SdtListItem](sdtlistitem/#constructor_1)(string, string) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayText](../../aspose.words.markup/sdtlistitem/displaytext/) { get; } | Ruft den Text ab, der im Ausführungsinhalt anstelle von angezeigt werden soll[`Value`](./value/) Attributinhalte für dieses Listenelement. |
| [Value](../../aspose.words.markup/sdtlistitem/value/) { get; } | Ruft den Wert dieses Listenelements ab. |

### Beispiele

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

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)


