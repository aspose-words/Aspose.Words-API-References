---
title: FrameFormat class
linktitle: FrameFormat class
articleTitle: FrameFormat class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.FrameFormat class. Represents frame related formatting for a paragraph."
type: docs
weight: 450
url: /nodejs-net/aspose.words/frameformat/
---

## FrameFormat class

Represents frame related formatting for a paragraph.


### Remarks

This object is always created. If a paragraph is a frame, then all properties will contain respective values, otherwise
all properties are set to their defaults.

Use [FrameFormat.isFrame](./isFrame/) to check whether paragraph is a frame.




### Properties

| Name | Description |
| --- | --- |
| [height](./height/) | Gets the height of the specified frame. |
| [heightRule](./heightRule/) | Gets the rule for determining the height of the specified frame. |
| [horizontalAlignment](./horizontalAlignment/) | Gets horizontal alignment of the specified frame. |
| [horizontalDistanceFromText](./horizontalDistanceFromText/) | Gets horizontal distance between a frame and the surrounding text, in points. |
| [horizontalPosition](./horizontalPosition/) | Gets horizontal distance between the edge of the frame and the item specified by the [FrameFormat.relativeHorizontalPosition](./relativeHorizontalPosition/) property. |
| [isFrame](./isFrame/) | Returns ``true`` if the paragraph is a frame. |
| [relativeHorizontalPosition](./relativeHorizontalPosition/) | Gets the relative horizontal position of a frame. |
| [relativeVerticalPosition](./relativeVerticalPosition/) | Gets the relative vertical position of a frame. |
| [verticalAlignment](./verticalAlignment/) | Gets vertical alignment of the specified frame. |
| [verticalDistanceFromText](./verticalDistanceFromText/) | Specifies vertical distance (in points) between a frame and the surrounding text. |
| [verticalPosition](./verticalPosition/) | Gets vertical distance between the edge of the frame and the item specified by the [FrameFormat.relativeVerticalPosition](./relativeVerticalPosition/) property. |
| [width](./width/) | Gets the width of the specified frame, in points. |

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

* module [Aspose.Words](../)

