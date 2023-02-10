---
title: Class TableStyle
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.TableStyle class. Represents a table style in C#.
type: docs
weight: 5990
url: /net/aspose.words/tablestyle/
---
## TableStyle class

Represents a table style.

To learn more, visit the [Working with Tables](https://docs.aspose.com/words/net/working-with-tables/) documentation article.

```csharp
public class TableStyle : Style
```

## Properties

| Name | Description |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Gets all aliases of this style. If style has no aliases then empty array of string is returned. |
| [Alignment](../../aspose.words/tablestyle/alignment/) { get; set; } | Specifies the alignment for the table style. |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages/) { get; set; } | Gets or sets a flag indicating whether text in a table row is allowed to split across a page break. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Specifies whether this style is automatically redefined based on the appropriate value. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Gets/sets the name of the style this style is based on. |
| [Bidi](../../aspose.words/tablestyle/bidi/) { get; set; } | Gets or sets whether this is a style for a right-to-left table. |
| [Borders](../../aspose.words/tablestyle/borders/) { get; } | Gets the collection of default cell borders for the style. |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding/) { get; set; } | Gets or sets the amount of space (in points) to add below the contents of table cells. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | True if this style is one of the built-in styles in MS Word. |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing/) { get; set; } | Gets or sets the amount of space (in points) between the cells. |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe/) { get; set; } | Gets or sets a number of columns to include in the banding when the style specifies odd/even columns banding. |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles/) { get; } | Collection of conditional styles that may be defined for this table style. |
| [Document](../../aspose.words/style/document/) { get; } | Gets the owner document. |
| [Font](../../aspose.words/style/font/) { get; } | Gets the character formatting of the style. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | True when the style is one of the built-in Heading styles. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI. |
| [LeftIndent](../../aspose.words/tablestyle/leftindent/) { get; set; } | Gets or sets the value that represents the left indent of a table. |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding/) { get; set; } | Gets or sets the amount of space (in points) to add to the left of the contents of table cells. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Gets the name of the [`Style`](../style/) linked to this one. Returns empty string if no styles are linked. |
| [List](../../aspose.words/style/list/) { get; } | Gets the list that defines formatting of this list style. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Provides access to the list formatting properties of a paragraph style. |
| [Name](../../aspose.words/style/name/) { get; set; } | Gets or sets the name of the style. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Gets the paragraph formatting of the style. |
| [RightPadding](../../aspose.words/tablestyle/rightpadding/) { get; set; } | Gets or sets the amount of space (in points) to add to the right of the contents of table cells. |
| [RowStripe](../../aspose.words/tablestyle/rowstripe/) { get; set; } | Gets or sets a number of rows to include in the banding when the style specifies odd/even row banding. |
| [Shading](../../aspose.words/tablestyle/shading/) { get; } | Gets a [`Shading`](../shading/) object that refers to the shading formatting for table cells. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Gets the locale independent style identifier for a built-in style. |
| [Styles](../../aspose.words/style/styles/) { get; } | Gets the collection of styles this style belongs to. |
| [TopPadding](../../aspose.words/tablestyle/toppadding/) { get; set; } | Gets or sets the amount of space (in points) to add above the contents of table cells. |
| [Type](../../aspose.words/style/type/) { get; } | Gets the style type (paragraph or character). |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment/) { get; set; } | Specifies the vertical alignment for the cells. |

## Methods

| Name | Description |
| --- | --- |
| [Equals](../../aspose.words/style/equals/)(Style) | Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared. |
| [Remove](../../aspose.words/style/remove/)() | Removes the specified style from the document. |

## Examples

Shows how to create custom style settings for the table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Setting the style properties of a table may affect the properties of the table itself.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### See Also

* class [Style](../style/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
