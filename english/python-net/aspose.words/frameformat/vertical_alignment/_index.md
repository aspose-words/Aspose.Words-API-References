---
title: FrameFormat.vertical_alignment property
linktitle: vertical_alignment property
articleTitle: vertical_alignment property
second_title: Aspose.Words for Python
description: "FrameFormat.vertical_alignment property. Gets vertical alignment of the specified frame."
type: docs
weight: 90
url: /python-net/aspose.words/frameformat/vertical_alignment/
---

## FrameFormat.vertical_alignment property

Gets vertical alignment of the specified frame.


### Examples

Shows how to get information about formatting properties of paragraphs that are frames.

```python
doc = aw.Document(MY_DIR + "Paragraph frame.docx")

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

* module [aspose.words](../../)
* class [FrameFormat](../)

