---
title: StyleCollection Class
linktitle: StyleCollection
articleTitle: StyleCollection
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.StyleCollection class, featuring a rich array of built-in and custom style objects to enhance your document's formatting and design.
type: docs
weight: 7000
url: /net/aspose.words/stylecollection/
---
## StyleCollection class

A collection of [`Style`](../style/) objects that represent both the built-in and user-defined styles in a document.

To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/net/working-with-styles-and-themes/) documentation article.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | Gets the number of styles in the collection. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | Gets document default text formatting. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | Gets document default paragraph formatting. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | Gets the owner document. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | Gets a style by name or alias. (3 indexers) |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(*[StyleType](../styletype/), string*) | Creates a new user defined style and adds it the collection. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(*[Style](../style/)*) | Copies a style into this collection. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | Removes all styles from the Quick Style Gallery panel. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | Gets an enumerator object that will enumerate styles in the alphabetical order of their names. |

## Examples

Shows how to create and use a paragraph style with list formatting.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a custom paragraph style.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Create a list and make sure the paragraphs that use this style will use this list.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Change the document builder's style to one that has no list formatting and write another paragraph.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### See Also

* class [Style](../style/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
