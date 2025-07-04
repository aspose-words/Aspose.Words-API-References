---
title: StyleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: Discover the StyleCollection Add method to effortlessly create and add custom user-defined styles to your collection, enhancing your design flexibility.
type: docs
weight: 60
url: /net/aspose.words/stylecollection/add/
---
## StyleCollection.Add method

Creates a new user defined style and adds it the collection.

```csharp
public Style Add(StyleType type, string name)
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | StyleType | A [`StyleType`](../../styletype/) value that specifies the type of the style to create. |
| name | String | Case sensitive name of the style to create. |

## Remarks

You can create character, paragraph or a list style.

When creating a list style, the style is created with default numbered list formatting (1 \ a \ i).

Throws an exception if a style with this name already exists.

## Examples

Shows how to add a Style to a document's styles collection.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Set default parameters for new styles that we may later add to this collection.
styles.DefaultFont.Name = "Courier New";
// If we add a style of the "StyleType.Paragraph", the collection will apply the values of
// its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Add a style, and then verify that it has the default settings.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.That(styles[4].Font.Name, Is.EqualTo("Courier New"));
Assert.That(styles["MyStyle"].ParagraphFormat.FirstLineIndent, Is.EqualTo(15.0));
```

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

### See Also

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
