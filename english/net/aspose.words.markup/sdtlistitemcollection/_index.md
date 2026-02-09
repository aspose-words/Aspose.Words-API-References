---
title: SdtListItemCollection Class
linktitle: SdtListItemCollection
articleTitle: SdtListItemCollection
second_title: Aspose.Words for .NET
description: Explore the Aspose.Words.Markup.SdtListItemCollection class for seamless access to SdtListItem elements, enhancing structured document management effortlessly.
type: docs
weight: 4760
url: /net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

Provides access to [`SdtListItem`](../sdtlistitem/) elements of a structured document tag.

To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/net/working-with-content-control-sdt/) documentation article.

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | Gets number of items in the collection. |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | Returns a [`SdtListItem`](../sdtlistitem/) object given its zero-based index in the collection. |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | Specifies currently selected value in this list. Null value allowed, meaning that no currently selected entry is associated with this list item collection. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(*[SdtListItem](../sdtlistitem/)*) | Adds an item to this collection. |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | Clears all items from this collection. |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(*int*) | Removes a list item at the specified index. |

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

Assert.That(listItems[0].Value, Is.EqualTo(listItems[0].DisplayText));

// Add 3 more list items. Initialize these items using a different constructor to the first item
// to display strings that are different from their values.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.That(listItems.Count, Is.EqualTo(4));

// The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
listItems.SelectedValue = listItems[3];

Assert.That(listItems.SelectedValue.Value, Is.EqualTo("Value 4"));

// Enumerate over the collection and print each element.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

// Remove the last list item. 
listItems.RemoveAt(3);

Assert.That(listItems.Count, Is.EqualTo(3));

// Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Use the "Clear" method to empty the entire drop-down item collection at once.
listItems.Clear();

Assert.That(listItems.Count, Is.EqualTo(0));
```

### See Also

* class [SdtListItem](../sdtlistitem/)
* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
