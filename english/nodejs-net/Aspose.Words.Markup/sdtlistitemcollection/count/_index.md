---
title: SdtListItemCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for NodeJs
description: "SdtListItemCollection.count property. Gets number of items in the collection."
type: docs
weight: 10
url: /nodejs-net/aspose.words.markup/sdtlistitemcollection/count/
---

## SdtListItemCollection.count property

Gets number of items in the collection.


```js
get count(): number
```

### Examples

Shows how to work with drop down-list structured document tags.

```js
let doc = new aw.Document();
let tag = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.DropDownList, aw.Markup.MarkupLevel.Block);
doc.firstSection.body.appendChild(tag);

// A drop-down list structured document tag is a form that allows the user to
// select an option from a list by left-clicking and opening the form in Microsoft Word.
// The "ListItems" property contains all list items, and each list item is an "SdtListItem".
let listItems = tag.listItems;
listItems.add(new aw.Markup.SdtListItem("Value 1"));

expect(listItems.at(0).value).toEqual(listItems.at(0).displayText);

// Add 3 more list items. Initialize these items using a different constructor to the first item
// to display strings that are different from their values.
listItems.add(new aw.Markup.SdtListItem("Item 2", "Value 2"));
listItems.add(new aw.Markup.SdtListItem("Item 3", "Value 3"));
listItems.add(new aw.Markup.SdtListItem("Item 4", "Value 4"));

expect(listItems.count).toEqual(4);

// The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
listItems.selectedValue = listItems.at(3);

expect(listItems.selectedValue.value).toEqual("Value 4");

// Enumerate over the collection and print each element.
for (let listItem of listItems) {
  if (listItem != null)
    console.log(`List item: ${listItem.displayText}, value: ${listItem.value}`);
}

// Remove the last list item. 
listItems.removeAt(3);

expect(listItems.count).toEqual(3);

// Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
listItems.selectedValue = listItems.at(1);

doc.save(base.artifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Use the "Clear" method to empty the entire drop-down item collection at once.
listItems.clear();

expect(listItems.count).toEqual(0);
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [SdtListItemCollection](../)

