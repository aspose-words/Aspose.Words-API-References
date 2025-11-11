---
title: TableStyle class
linktitle: TableStyle class
articleTitle: TableStyle class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.TableStyle class. Represents a table style"
type: docs
weight: 1370
url: /nodejs-net/aspose.words/tablestyle/
---

## TableStyle class

Represents a table style.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/nodejs-net/working-with-tables/) documentation article.




**Inheritance:** [TableStyle](./) → [Style](../style/)

### Properties

| Name | Description |
| --- | --- |
| [aliases](../style/aliases/) | Gets all aliases of this style. If style has no aliases then empty array of string is returned.<br>(Inherited from [Style](../style/)) |
| [alignment](./alignment/) | Specifies the alignment for the table style. |
| [allowBreakAcrossPages](./allowBreakAcrossPages/) | Gets or sets a flag indicating whether text in a table row is allowed to split across a page break. |
| [automaticallyUpdate](../style/automaticallyUpdate/) | Specifies whether this style is automatically redefined based on the appropriate value.<br>(Inherited from [Style](../style/)) |
| [baseStyleName](../style/baseStyleName/) | Gets/sets the name of the style this style is based on.<br>(Inherited from [Style](../style/)) |
| [borders](./borders/) | Gets the collection of default cell borders for the style. |
| [bottomPadding](./bottomPadding/) | Gets or sets the amount of space (in points) to add below the contents of table cells. |
| [builtIn](../style/builtIn/) | True if this style is one of the built-in styles in MS Word.<br>(Inherited from [Style](../style/)) |
| [cellSpacing](./cellSpacing/) | Gets or sets the amount of space (in points) between the cells. |
| [columnStripe](./columnStripe/) | Gets or sets a number of columns to include in the banding when the style specifies odd/even columns banding. |
| [conditionalStyles](./conditionalStyles/) | Collection of conditional styles that may be defined for this table style. |
| [document](../style/document/) | Gets the owner document.<br>(Inherited from [Style](../style/)) |
| [font](../style/font/) | Gets the character formatting of the style.<br>(Inherited from [Style](../style/)) |
| [isHeading](../style/isHeading/) | True when the style is one of the built-in Heading styles.<br>(Inherited from [Style](../style/)) |
| [isQuickStyle](../style/isQuickStyle/) | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.<br>(Inherited from [Style](../style/)) |
| [leftIndent](./leftIndent/) | Gets or sets the value that represents the left indent of a table. |
| [leftPadding](./leftPadding/) | Gets or sets the amount of space (in points) to add to the left of the contents of table cells. |
| [linkedStyleName](../style/linkedStyleName/) | Gets/sets the name of the [Style](../style/) linked to this one. Returns empty string if no styles are linked.<br>(Inherited from [Style](../style/)) |
| [list](../style/list/) | Gets the list that defines formatting of this list style.<br>(Inherited from [Style](../style/)) |
| [listFormat](../style/listFormat/) | Provides access to the list formatting properties of a paragraph style.<br>(Inherited from [Style](../style/)) |
| [locked](../style/locked/) | Specifies whether this style is locked.<br>(Inherited from [Style](../style/)) |
| [name](../style/name/) | Gets or sets the name of the style.<br>(Inherited from [Style](../style/)) |
| [nextParagraphStyleName](../style/nextParagraphStyleName/) | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style.<br>(Inherited from [Style](../style/)) |
| [paragraphFormat](../style/paragraphFormat/) | Gets the paragraph formatting of the style.<br>(Inherited from [Style](../style/)) |
| [priority](../style/priority/) | Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane.<br>(Inherited from [Style](../style/)) |
| [rightPadding](./rightPadding/) | Gets or sets the amount of space (in points) to add to the right of the contents of table cells. |
| [rowStripe](./rowStripe/) | Gets or sets a number of rows to include in the banding when the style specifies odd/even row banding. |
| [semiHidden](../style/semiHidden/) | Gets/sets whether the style hides from the Styles gallery and from the Styles task pane.<br>(Inherited from [Style](../style/)) |
| [shading](./shading/) | Gets a [Shading](../shading/) object that refers to the shading formatting for table cells. |
| [styleIdentifier](../style/styleIdentifier/) | Gets the locale independent style identifier for a built-in style.<br>(Inherited from [Style](../style/)) |
| [styles](../style/styles/) | Gets the collection of styles this style belongs to.<br>(Inherited from [Style](../style/)) |
| [topPadding](./topPadding/) | Gets or sets the amount of space (in points) to add above the contents of table cells. |
| [type](../style/type/) | Gets the style type (paragraph or character).<br>(Inherited from [Style](../style/)) |
| [unhideWhenUsed](../style/unhideWhenUsed/) | Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane. True when the used style should be shown in the Styles gallery.<br>(Inherited from [Style](../style/)) |
| [verticalAlignment](./verticalAlignment/) | Specifies the vertical alignment for the cells. |

### Methods

| Name | Description |
| --- | --- |
|[ asTableStyle()](../style/asTableStyle/#default) | <br>(Inherited from [Style](../style/)) |
|[ equals(style)](../style/equals/#style) | Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared.<br>(Inherited from [Style](../style/)) |
|[ remove()](../style/remove/#default) | Removes the specified style from the document.<br>(Inherited from [Style](../style/)) |

### Examples

Shows how to create custom style settings for the table.

```js
let doc = new aw.Document();
    let builder = new aw.DocumentBuilder(doc);
 
    let table = builder.startTable();
    builder.insertCell();
    builder.write("Name");
    builder.insertCell();
    builder.write("مرحبًا");
    builder.endRow();
    builder.insertCell();
    builder.insertCell();
    builder.endTable();
 
    let tableStyle = doc.styles.add(aw.StyleType.Table, "MyTableStyle1").asTableStyle();
    tableStyle.allowBreakAcrossPages = true;
    tableStyle.bidi = true;
    tableStyle.cellSpacing = 5;
    tableStyle.bottomPadding = 20;
    tableStyle.leftPadding = 5;
    tableStyle.rightPadding = 10;
    tableStyle.topPadding = 20;
    tableStyle.shading.backgroundPatternColor = "#FAEBD7";
    tableStyle.borders.color = "#0000FF";
    tableStyle.borders.lineStyle = aw.LineStyle.DotDash;
    tableStyle.verticalAlignment = aw.Tables.CellVerticalAlignment.Center;

    table.style = tableStyle;

    // Setting the style properties of a table may affect the properties of the table itself.
    //expect(table.bidi).toEqual(true);
    expect(table.cellSpacing).toEqual(5.0);
    expect(table.styleName).toEqual("MyTableStyle1");

    doc.save(base.artifactsDir + "Table.TableStyleCreation.docx");
```

### See Also

* module [Aspose.Words](../)
* class [Style](../style/)

