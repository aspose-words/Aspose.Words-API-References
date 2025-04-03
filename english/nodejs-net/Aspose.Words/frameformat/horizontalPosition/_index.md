---
title: FrameFormat.horizontalPosition property
linktitle: horizontalPosition property
articleTitle: horizontalPosition property
second_title: Aspose.Words for NodeJs
description: "FrameFormat.horizontalPosition property. Gets horizontal distance between the edge of the frame and the item specified by the [FrameFormat.relativeHorizontalPosition](../relativeHorizontalPosition/) property."
type: docs
weight: 50
url: /nodejs-net/aspose.words/frameformat/horizontalPosition/
---

## FrameFormat.horizontalPosition property

Gets horizontal distance between the edge of the frame and the item specified by the [FrameFormat.relativeHorizontalPosition](../relativeHorizontalPosition/) property.



```js
get horizontalPosition(): number
```

### Examples

Shows how to get information about formatting properties of paragraphs that are frames.

```js
let doc = new aw.Document(base.myDir + "Paragraph frame.docx");
let paragraphFrame = doc.firstSection.body.paragraphs.toArray().filter(p => p.frameFormat.isFrame).at(0);

expect(paragraphFrame.frameFormat.width).toEqual(233.3);
expect(paragraphFrame.frameFormat.height).toEqual(138.8);
expect(paragraphFrame.frameFormat.heightRule).toEqual(aw.HeightRule.AtLeast);
expect(paragraphFrame.frameFormat.horizontalAlignment).toEqual(aw.Drawing.HorizontalAlignment.Default);
expect(paragraphFrame.frameFormat.verticalAlignment).toEqual(aw.Drawing.VerticalAlignment.Default);
expect(paragraphFrame.frameFormat.horizontalPosition).toEqual(34.05);
expect(paragraphFrame.frameFormat.relativeHorizontalPosition).toEqual(aw.Drawing.RelativeHorizontalPosition.Page);
expect(paragraphFrame.frameFormat.horizontalDistanceFromText).toEqual(9.0);
expect(paragraphFrame.frameFormat.verticalPosition).toEqual(20.5);
expect(paragraphFrame.frameFormat.relativeVerticalPosition).toEqual(aw.Drawing.RelativeVerticalPosition.Paragraph);
expect(paragraphFrame.frameFormat.verticalDistanceFromText).toEqual(0.0);
```

### See Also

* module [Aspose.Words](../../)
* class [FrameFormat](../)

