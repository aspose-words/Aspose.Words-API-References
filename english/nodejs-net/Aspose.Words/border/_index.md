---
title: Border class
linktitle: Border class
articleTitle: Border class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Border class. Represents a border of an object"
type: docs
weight: 90
url: /nodejs-net/aspose.words/border/
---

## Border class

Represents a border of an object.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/nodejs-net/programming-with-documents/) documentation article.




### Remarks

Borders can be applied to various document elements including paragraph,
run of text inside a paragraph or a table cell.




**Inheritance:** [Border](./) → [InternableComplexAttr](../internablecomplexattr/)

### Properties

| Name | Description |
| --- | --- |
| [color](./color/) | Gets or sets the border color. |
| [distanceFromText](./distanceFromText/) | Gets or sets distance of the border from text or from the page edge in points. |
| [isVisible](./isVisible/) | Returns ``true`` if the [Border.lineStyle](./lineStyle/) is not [LineStyle.None](../linestyle/#None). |
| [lineStyle](./lineStyle/) | Gets or sets the border style. |
| [lineWidth](./lineWidth/) | Gets or sets the border width in points. |
| [shadow](./shadow/) | Gets or sets a value indicating whether the border has a shadow. |
| [themeColor](./themeColor/) | Gets or sets the theme color in the applied color scheme that is associated with this Border object. |
| [tintAndShade](./tintAndShade/) | Gets or sets a double value that lightens or darkens a color. |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormatting()](./clearFormatting/#default) | Resets border properties to default values. |
|[ equals(rhs)](./equals/#border) | Determines whether the specified border is equal in value to the current border. |

### Examples

Shows how to insert a string surrounded by a border into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.border.color = "#008000";
builder.font.border.lineWidth = 2.5;
builder.font.border.lineStyle = aw.LineStyle.DashDotStroker;

builder.write("Text surrounded by green border.");

doc.save(base.artifactsDir + "Border.FontBorder.docx");
```

Shows how to insert a paragraph with a top border.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let topBorder = builder.paragraphFormat.borders.top;
topBorder.lineWidth = 4.0;
topBorder.lineStyle = aw.LineStyle.DashSmallGap;
// Set ThemeColor only when LineWidth or LineStyle setted.
topBorder.themeColor = aw.Themes.ThemeColor.Accent1;
topBorder.tintAndShade = 0.25;

builder.writeln("Text with a top border.");

doc.save(base.artifactsDir + "Border.ParagraphTopBorder.docx");
```

### See Also

* module [Aspose.Words](../)
* class [InternableComplexAttr](../internablecomplexattr/)

