---
title: ListItems
second_title: Aspose.Words for .NET API Reference
description: StructuredDocumentTag property. Gets SdtListItemCollection associated with this SDT in C#.
type: docs
weight: 180
url: /net/aspose.words.markup/structureddocumenttag/listitems/
---
## StructuredDocumentTag.ListItems property

Gets [`SdtListItemCollection`](../../sdtlistitemcollection/) associated with this **SDT**.

```csharp
public SdtListItemCollection ListItems { get; }
```

## Remarks

Accessing this property will only work for ComboBox or DropDownList SDT types.

For all other SDT types exception will occur.

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

* class [SdtListItemCollection](../../sdtlistitemcollection/)
* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../structureddocumenttag/)
* assembly [Aspose.Words](../../../)
