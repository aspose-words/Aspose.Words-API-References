---
title: Add
second_title: Aspose.Words for .NET API Reference
description: ListCollection method. Creates a new list based on a predefined template and adds it to the collection of lists in the document in C#.
type: docs
weight: 40
url: /net/aspose.words.lists/listcollection/add/
---
## Add(ListTemplate) {#add}

Creates a new list based on a predefined template and adds it to the collection of lists in the document.

```csharp
public List Add(ListTemplate listTemplate)
```

| Parameter | Type | Description |
| --- | --- | --- |
| listTemplate | ListTemplate | The template of the list. |

### Return Value

The newly created list.

## Remarks

Aspose.Words list templates correspond to the 21 list templates available in the Bullets and Numbering dialog box in Microsoft Word 2003.

All lists created using this method have 9 list levels.

## Examples

Shows how to create a list by applying a new list format to a collection of paragraphs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));

List list = doc.Lists.Add(ListTemplate.NumberUppercaseLetterDot);

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = list;
    paragraph.ListFormat.ListLevelNumber = 1;
}

Assert.AreEqual(3, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));
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

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* namespace [Aspose.Words.Lists](../../listcollection/)
* assembly [Aspose.Words](../../../)

---

## Add(Style) {#add_1}

Creates a new list that references a list style and adds it to the collection of lists in the document.

```csharp
public List Add(Style listStyle)
```

| Parameter | Type | Description |
| --- | --- | --- |
| listStyle | Style | The list style. |

### Return Value

The newly created list.

## Remarks

The newly created list references the list style. If you change the properties of the list style, it is reflected in the properties of the list. Vice versa, if you change the properties of the list, it is reflected in the properties of the list style.

## Examples

Shows how to create a list style and use it in a document.

```csharp
Document doc = new Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// We can contain an entire List object within a style.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Change the appearance of all list levels in our list.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Create another list from a list within a style.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Add some list items that our list will format.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Create and apply another list based on the list style.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### See Also

* class [List](../../list/)
* class [Style](../../../aspose.words/style/)
* class [ListCollection](../)
* namespace [Aspose.Words.Lists](../../listcollection/)
* assembly [Aspose.Words](../../../)
