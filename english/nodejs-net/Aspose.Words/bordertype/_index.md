---
title: BorderType enumeration
linktitle: BorderType enumeration
articleTitle: BorderType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.BorderType enumeration. Specifies sides of a border"
type: docs
weight: 110
url: /nodejs-net/Aspose.Words/bordertype/
---

## BorderType enumeration

Specifies sides of a border.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/nodejs-net/programming-with-documents/) documentation article.




### Members

| Name | Description |
| --- | --- |
| None | Default value. |
| Bottom | Specifies the bottom border of a paragraph or a table cell. |
| Left | Specifies the left border of a paragraph or a table cell. |
| Right | Specifies the right border of a paragraph or a table cell. |
| Top | Specifies the top border of a paragraph or a table cell. |
| Horizontal | Specifies the horizontal border between cells in a table or between conforming paragraphs. |
| Vertical | Specifies the vertical border between cells in a table. |
| DiagonalDown | Specifies the diagonal border in a table cell. |
| DiagonalUp | Specifies the diagonal border in a table cell. |

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

