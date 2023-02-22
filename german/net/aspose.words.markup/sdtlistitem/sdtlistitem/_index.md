---
title: SdtListItem.SdtListItem
second_title: Aspose.Words für .NET-API-Referenz
description: SdtListItem constructeur. Initialisiert eine neue Instanz dieser Klasse.
type: docs
weight: 10
url: /de/net/aspose.words.markup/sdtlistitem/sdtlistitem/
---
## SdtListItem(string, string) {#constructor_1}

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public SdtListItem(string displayText, string value)
```

### Beispiele

Zeigt, wie mit Dropdown-Listen-strukturierten Dokument-Tags gearbeitet wird.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Ein strukturiertes Dokument-Tag mit Dropdown-Liste ist ein Formular, das dem Benutzer dies ermöglicht
// Wählen Sie eine Option aus einer Liste aus, indem Sie mit der linken Maustaste klicken und das Formular in Microsoft Word öffnen.
// Die Eigenschaft "ListItems" enthält alle Listenelemente, und jedes Listenelement ist ein "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Drei weitere Listenelemente hinzufügen. Initialisieren Sie diese Elemente mit einem anderen Konstruktor als das erste Element
// um Strings anzuzeigen, die sich von ihren Werten unterscheiden.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// Die Dropdown-Liste zeigt das erste Element an. Weisen Sie dem "SelectedValue" einen anderen Listeneintrag zu, um ihn anzuzeigen.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Auflistung über die Sammlung und jedes Element drucken.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Das letzte Listenelement entfernen.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Da unser Dropdown-Steuerelement standardmäßig so eingestellt ist, dass es das entfernte Element anzeigt, geben Sie ihm ein Element zum Anzeigen, das vorhanden ist.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Verwenden Sie die "Clear"-Methode, um die gesamte Dropdown-Elementsammlung auf einmal zu leeren.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Siehe auch

* class [SdtListItem](../)
* namensraum [Aspose.Words.Markup](../../sdtlistitem/)
* Montage [Aspose.Words](../../../)

---

## SdtListItem(string) {#constructor}

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public SdtListItem(string value)
```

### Beispiele

Zeigt, wie mit Dropdown-Listen-strukturierten Dokument-Tags gearbeitet wird.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Ein strukturiertes Dokument-Tag mit Dropdown-Liste ist ein Formular, das dem Benutzer dies ermöglicht
// Wählen Sie eine Option aus einer Liste aus, indem Sie mit der linken Maustaste klicken und das Formular in Microsoft Word öffnen.
// Die Eigenschaft "ListItems" enthält alle Listenelemente, und jedes Listenelement ist ein "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Drei weitere Listenelemente hinzufügen. Initialisieren Sie diese Elemente mit einem anderen Konstruktor als das erste Element
// um Strings anzuzeigen, die sich von ihren Werten unterscheiden.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// Die Dropdown-Liste zeigt das erste Element an. Weisen Sie dem "SelectedValue" einen anderen Listeneintrag zu, um ihn anzuzeigen.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Auflistung über die Sammlung und jedes Element drucken.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Das letzte Listenelement entfernen.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Da unser Dropdown-Steuerelement standardmäßig so eingestellt ist, dass es das entfernte Element anzeigt, geben Sie ihm ein Element zum Anzeigen, das vorhanden ist.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Verwenden Sie die "Clear"-Methode, um die gesamte Dropdown-Elementsammlung auf einmal zu leeren.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Siehe auch

* class [SdtListItem](../)
* namensraum [Aspose.Words.Markup](../../sdtlistitem/)
* Montage [Aspose.Words](../../../)


