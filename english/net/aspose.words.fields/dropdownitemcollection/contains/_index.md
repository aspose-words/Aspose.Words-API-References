---
title: DropDownItemCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words for .NET
description: Discover if a DropDownItemCollection includes your specified value with our efficient Contains method. Enhance your data management effortlessly!
type: docs
weight: 50
url: /net/aspose.words.fields/dropdownitemcollection/contains/
---
## DropDownItemCollection.Contains method

Determines whether the collection contains the specified value.

```csharp
public bool Contains(string value)
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | String | Case-sensitive value to locate. |

### Return Value

`true` if the item is found in the collection; otherwise, `false`.

## Examples

Shows how to insert a combo box field, and edit the elements in its item collection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a combo box, and then verify its collection of drop-down items.
// In Microsoft Word, the user will click the combo box,
// and then choose one of the items of text in the collection to display.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.That(dropDownItems.Count, Is.EqualTo(3));
Assert.That(dropDownItems[0], Is.EqualTo("One"));
Assert.That(dropDownItems.IndexOf("Two"), Is.EqualTo(1));
Assert.That(dropDownItems.Contains("Three"), Is.True);

// There are two ways of adding a new item to an existing collection of drop-down box items.
// 1 -  Append an item to the end of the collection:
dropDownItems.Add("Four");

// 2 -  Insert an item before another item at a specified index:
dropDownItems.Insert(3, "Three and a half");

Assert.That(dropDownItems.Count, Is.EqualTo(5));

// Iterate over the collection and print every element.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// There are two ways of removing elements from a collection of drop-down items.
// 1 -  Remove an item with contents equal to the passed string:
dropDownItems.Remove("Four");

// 2 -  Remove an item at an index:
dropDownItems.RemoveAt(3);

Assert.That(dropDownItems.Count, Is.EqualTo(3));
Assert.That(dropDownItems.Contains("Three and a half"), Is.False);
Assert.That(dropDownItems.Contains("Four"), Is.False);

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Empty the whole collection of drop-down items.
dropDownItems.Clear();
```

### See Also

* class [DropDownItemCollection](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
