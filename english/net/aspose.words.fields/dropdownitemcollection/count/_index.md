---
title: DropDownItemCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: Discover the DropDownItemCollection Count property, which efficiently retrieves the total number of items in your collection for streamlined data management.
type: docs
weight: 10
url: /net/aspose.words.fields/dropdownitemcollection/count/
---
## DropDownItemCollection.Count property

Gets the number of elements contained in the collection.

```csharp
public int Count { get; }
```

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

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// There are two ways of adding a new item to an existing collection of drop-down box items.
// 1 -  Append an item to the end of the collection:
dropDownItems.Add("Four");

// 2 -  Insert an item before another item at a specified index:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Iterate over the collection and print every element.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// There are two ways of removing elements from a collection of drop-down items.
// 1 -  Remove an item with contents equal to the passed string:
dropDownItems.Remove("Four");

// 2 -  Remove an item at an index:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Empty the whole collection of drop-down items.
dropDownItems.Clear();
```

### See Also

* class [DropDownItemCollection](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
