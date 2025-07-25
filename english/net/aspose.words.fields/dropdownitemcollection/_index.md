---
title: DropDownItemCollection Class
linktitle: DropDownItemCollection
articleTitle: DropDownItemCollection
second_title: Aspose.Words for .NET
description: Explore the Aspose.Words.Fields.DropDownItemCollection class—your go-to solution for managing dropdown items in form fields effortlessly!
type: docs
weight: 1900
url: /net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

A collection of strings that represent all the items in a drop-down form field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | Gets the number of elements contained in the collection. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | Gets or sets the element at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(*string*) | Adds a string to the end of the collection. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | Removes all elements from the collection. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(*string*) | Determines whether the collection contains the specified value. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(*string*) | Returns the zero-based index of the specified value in the collection. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(*int, string*) | Inserts a string into the collection at the specified index. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(*string*) | Removes the specified value from the collection. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(*int*) | Removes a value at the specified index. |

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

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
