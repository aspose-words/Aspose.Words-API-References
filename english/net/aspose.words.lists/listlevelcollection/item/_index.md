---
title: ListLevelCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Access list levels effortlessly with the ListLevelCollection Item property. Retrieve any level by index for seamless document formatting.
type: docs
weight: 20
url: /net/aspose.words.lists/listlevelcollection/item/
---
## ListLevelCollection indexer

Gets a list level by index.

```csharp
public ListLevel this[int index] { get; set; }
```

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

Assert.That(list1.IsListStyleDefinition, Is.True);
Assert.That(list1.IsListStyleReference, Is.False);
Assert.That(list1.IsMultiLevel, Is.True);
Assert.That(list1.Style, Is.EqualTo(listStyle));

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

Assert.That(list2.IsListStyleDefinition, Is.False);
Assert.That(list2.IsListStyleReference, Is.True);
Assert.That(list2.Style, Is.EqualTo(listStyle));

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

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```csharp
Document doc = new Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize the first two of its list levels.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// This NumberFormat value will create star-shaped bullet list symbols.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Create paragraphs and apply both list levels of our custom list formatting to them.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### See Also

* class [ListLevel](../../listlevel/)
* class [ListLevelCollection](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)
