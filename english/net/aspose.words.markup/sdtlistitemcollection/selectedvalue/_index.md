---
title: SdtListItemCollection.SelectedValue
linktitle: SelectedValue
articleTitle: SelectedValue
second_title: Aspose.Words for .NET
description: SdtListItemCollection SelectedValue property. Specifies currently selected value in this list. Null value allowed meaning that no currently selected entry is associated with this list item collection in C#.
type: docs
weight: 30
url: /net/aspose.words.markup/sdtlistitemcollection/selectedvalue/
---
## SdtListItemCollection.SelectedValue property

Specifies currently selected value in this list. Null value allowed, meaning that no currently selected entry is associated with this list item collection.

```csharp
public SdtListItem SelectedValue { get; set; }
```

## Examples

Shows how to work with drop down-list structured document tags.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// A drop-down list structured document tag is a form that allows the user to
// select an option from a list by left-clicking and opening the form in Microsoft Word.
// The "ListItems" property contains all list items, and each list item is an "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Add 3 more list items. Initialize these items using a different constructor to the first item
// to display strings that are different from their values.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Enumerate over the collection and print each element.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

// Remove the last list item. 
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Use the "Clear" method to empty the entire drop-down item collection at once.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### See Also

* class [SdtListItem](../../sdtlistitem/)
* class [SdtListItemCollection](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
