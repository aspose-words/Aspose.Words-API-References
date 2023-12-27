---
title: Style Class
linktitle: Style
articleTitle: Style
second_title: Aspose.Words for .NET
description: Aspose.Words.Style class. Represents a single builtin or userdefined style in C#.
type: docs
weight: 6270
url: /net/aspose.words/style/
---
## Style class

Represents a single built-in or user-defined style.

To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/net/working-with-styles-and-themes/) documentation article.

```csharp
public class Style
```

## Properties

| Name | Description |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Gets all aliases of this style. If style has no aliases then empty array of string is returned. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Specifies whether this style is automatically redefined based on the appropriate value. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Gets/sets the name of the style this style is based on. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | True if this style is one of the built-in styles in MS Word. |
| [Document](../../aspose.words/style/document/) { get; } | Gets the owner document. |
| [Font](../../aspose.words/style/font/) { get; } | Gets the character formatting of the style. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | True when the style is one of the built-in Heading styles. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Gets the name of the `Style` linked to this one. Returns empty string if no styles are linked. |
| [List](../../aspose.words/style/list/) { get; } | Gets the list that defines formatting of this list style. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Provides access to the list formatting properties of a paragraph style. |
| [Locked](../../aspose.words/style/locked/) { get; set; } | Specifies whether this style is locked. |
| [Name](../../aspose.words/style/name/) { get; set; } | Gets or sets the name of the style. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Gets the paragraph formatting of the style. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Gets the locale independent style identifier for a built-in style. |
| [Styles](../../aspose.words/style/styles/) { get; } | Gets the collection of styles this style belongs to. |
| [Type](../../aspose.words/style/type/) { get; } | Gets the style type (paragraph or character). |

## Methods

| Name | Description |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(*Style*) | Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared. |
| [Remove](../../aspose.words/style/remove/)() | Removes the specified style from the document. |

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

Shows how to create and apply a custom style.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Automatically redefine style.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Apply one of the styles from the document to the paragraph that the document builder is creating.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Remove our custom style from the document's styles collection.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Any text that used a removed style reverts to the default formatting.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
