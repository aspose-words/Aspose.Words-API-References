---
title: FrameFormat class
linktitle: FrameFormat class
articleTitle: FrameFormat class
second_title: Aspose.Words for Python
description: "aspose.words.FrameFormat class. Represents frame related formatting for a paragraph."
type: docs
weight: 470
url: /python-net/aspose.words/frameformat/
---

## FrameFormat class

Represents frame related formatting for a paragraph.


### Remarks

This object is always created. If a paragraph is a frame, then all properties will contain respective values, otherwise
all properties are set to their defaults.

Use [FrameFormat.is_frame](./is_frame/) to check whether paragraph is a frame.




### Properties

| Name | Description |
| --- | --- |
| [height](./height/) | Gets the height of the specified frame. |
| [height_rule](./height_rule/) | Gets the rule for determining the height of the specified frame. |
| [horizontal_alignment](./horizontal_alignment/) | Gets horizontal alignment of the specified frame. |
| [horizontal_distance_from_text](./horizontal_distance_from_text/) | Gets horizontal distance between a frame and the surrounding text, in points. |
| [horizontal_position](./horizontal_position/) | Gets horizontal distance between the edge of the frame and the item specified by the [FrameFormat.relative_horizontal_position](./relative_horizontal_position/) property. |
| [is_frame](./is_frame/) | Returns ``True`` if the paragraph is a frame. |
| [relative_horizontal_position](./relative_horizontal_position/) | Gets the relative horizontal position of a frame. |
| [relative_vertical_position](./relative_vertical_position/) | Gets the relative vertical position of a frame. |
| [vertical_alignment](./vertical_alignment/) | Gets vertical alignment of the specified frame. |
| [vertical_distance_from_text](./vertical_distance_from_text/) | Specifies vertical distance (in points) between a frame and the surrounding text. |
| [vertical_position](./vertical_position/) | Gets vertical distance between the edge of the frame and the item specified by the [FrameFormat.relative_vertical_position](./relative_vertical_position/) property. |
| [width](./width/) | Gets the width of the specified frame, in points. |

### Examples

Shows how to get information about formatting properties of paragraphs that are frames.

```python
doc = aw.Document(MY_DIR + 'Paragraph frame.docx')
for paragraph in doc.first_section.body.paragraphs:
    paragraph = paragraph.as_paragraph()
    if paragraph.frame_format.is_frame:
        paragraph_frame = paragraph
        break
self.assertEqual(233.3, paragraph_frame.frame_format.width)
self.assertEqual(138.8, paragraph_frame.frame_format.height)
self.assertEqual(aw.HeightRule.AT_LEAST, paragraph_frame.frame_format.height_rule)
self.assertEqual(aw.drawing.HorizontalAlignment.DEFAULT, paragraph_frame.frame_format.horizontal_alignment)
self.assertEqual(aw.drawing.VerticalAlignment.DEFAULT, paragraph_frame.frame_format.vertical_alignment)
self.assertEqual(34.05, paragraph_frame.frame_format.horizontal_position)
self.assertEqual(aw.drawing.RelativeHorizontalPosition.PAGE, paragraph_frame.frame_format.relative_horizontal_position)
self.assertEqual(9.0, paragraph_frame.frame_format.horizontal_distance_from_text)
self.assertEqual(20.5, paragraph_frame.frame_format.vertical_position)
self.assertEqual(aw.drawing.RelativeVerticalPosition.PARAGRAPH, paragraph_frame.frame_format.relative_vertical_position)
self.assertEqual(0.0, paragraph_frame.frame_format.vertical_distance_from_text)
```

### See Also

* module [aspose.words](../)

