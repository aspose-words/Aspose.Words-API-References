---
title: BorderCollection class
linktitle: BorderCollection class
articleTitle: BorderCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.BorderCollection class. A collection of [Border](../border/) objects"
type: docs
weight: 100
url: /nodejs-net/Aspose.Words/bordercollection/
---

## BorderCollection class

A collection of [Border](../border/) objects.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/nodejs-net/programming-with-documents/) documentation article.




### Remarks

Different document elements have different borders.
For example, [ParagraphFormat](../paragraphformat/) has [BorderCollection.bottom](./bottom/), [BorderCollection.left](./left/), [BorderCollection.right](./right/) and [BorderCollection.top](./top/) borders.
You can specify different formatting for each border independently or
enumerate through all borders and apply same formatting.



### Properties

| Name | Description |
| --- | --- |
| [bottom](./bottom/) | Gets the bottom border. |
| [color](./color/) | Gets or sets the border color. |
| [count](./count/) | Gets the number of borders in the collection. |
| [distanceFromText](./distanceFromText/) | Gets or sets distance of the border from text in points. |
| [horizontal](./horizontal/) | Gets the horizontal border that is used between cells or conforming paragraphs. |
| [left](./left/) | Gets the left border. |
| [lineStyle](./lineStyle/) | Gets or sets the border style. |
| [lineWidth](./lineWidth/) | Gets or sets the border width in points. |
| [right](./right/) | Gets the right border. |
| [shadow](./shadow/) | Gets or sets a value indicating whether the border has a shadow. |
| [this[]](./this[]/) |  |
| [this[]](./this[]/) |  |
| [top](./top/) | Gets the top border. |
| [vertical](./vertical/) | Gets the vertical border that is used between cells. |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormatting()](./clearFormatting/#default) | Removes all borders of an object. |
|[ equals(brColl)](./equals/#bordercollection) | Compares collections of borders. |

### Examples

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

