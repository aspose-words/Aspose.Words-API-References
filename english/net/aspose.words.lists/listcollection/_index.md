---
title: "ListCollection"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 3210
url: /net/aspose.words.lists/listcollection/
---
## ListCollection class

Stores and manages formatting of bulleted and numbered lists used in a document.

```csharp
public class ListCollection : IEnumerable<List>
```

## Public Members

| Name | Description |
| --- | --- |
| [Count](count) { get; } | Gets the count of numbered and bulleted lists in the document. |
| [Document](document) { get; } | Gets the owner document. |
| [Item](item) { get; } | Gets a list by index. |
| [Add](add)(…) | Creates a new list based on a predefined template and adds it to the collection of lists in the document. (2 methods) |
| [AddCopy](addcopy)(…) | Creates a new list by copying the specified list and adding it to the collection of lists in the document. |
| [GetEnumerator](getenumerator)() | Gets the enumerator object that will enumerate lists in the document. |
| [GetListByListId](getlistbylistid)(…) | Gets a list by a list identifier. |

### Remarks

A list in a Microsoft Word document is a set of list formatting properties. The formatting of the lists is stored in the [`ListCollection`](../listcollection) collection separately from the paragraphs of text.You do not create objects of this class. There is always only one [`ListCollection`](../listcollection) object per document and it is accessible via the [`Lists`](../../aspose.words/documentbase/lists) property.To create a new list based on a predefined list template or based on a list style, use the [`Add`](./add) method.To create a new list with formatting identical to an existing list, use the [`AddCopy`](./addcopy) method.To make a paragraph bulleted or numbered, you need to apply list formatting to a paragraph by assigning a [`List`](../list) object to the [`List`](../listformat/list) property of [`ListFormat`](../listformat).To remove list formatting from a paragraph, use the [`RemoveNumbers`](../listformat/removenumbers) method.If you know a bit about WordprocessingML, then you might know it defines separate concepts for "list" and "list definition". This exactly corresponds to how list formatting is stored in a Microsoft Word document at the low level. List definition is like a "schema" and list is like an instance of a list definition.To simplify programming model, Aspose.Words hides the distinction between list and list definition in much the same way like Microsoft Word hides this in its user interface. This allows you to concentrate more on how you want your document to look like, rather than building low-level objects to satisfy requirements of the Microsoft Word file format.It is not possible to delete lists once they are created in the current version of Aspose.Words. This is similar to Microsoft Word where user does not have explicit control over list definitions.

### Examples

Shows how to create a document with a sample of all the lists from another document.

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
}
```

Shows how to restart numbering in a list by copying a list.

```csharp
Document doc = new Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize its first list level.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Apply our list to some paragraphs.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// We can add a copy of an existing list to the document's list collection
// to create a similar list without making changes to the original.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Apply the second list to new paragraphs.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Shows how to work with list levels.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create using a document builder.
// 1 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// By setting the "ListLevelNumber" property, we can increase the list level
// to begin a self-contained sub-list at the current list item.
// The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
// Deeper list levels use letters and lowercase Roman numerals. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
// Deeper levels of this list will use different symbols, such as "■" and "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### See Also

* class [List](../list)
* namespace [Aspose.Words.Lists](../../aspose.words.lists)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
