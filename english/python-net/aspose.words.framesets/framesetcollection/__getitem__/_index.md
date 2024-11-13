---
title: FramesetCollection indexer
linktitle: FramesetCollection indexer
articleTitle: FramesetCollection indexer
second_title: Aspose.Words for Python
description: "FramesetCollection indexer. Gets a frame or frames page at the specified index."
type: docs
weight: 20
url: /python-net/aspose.words.framesets/framesetcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets a frame or frames page at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to access frames on-page.

```python
# Document contains several frames with links to other documents.
doc = aw.Document(file_name=MY_DIR + 'Frameset.docx')
self.assertEqual(3, doc.frameset.child_framesets.count)
# We can check the default URL (a web page URL or local document) or if the frame is an external resource.
self.assertEqual('https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx', doc.frameset.child_framesets[0].child_framesets[0].frame_default_url)
self.assertTrue(doc.frameset.child_framesets[0].child_framesets[0].is_frame_link_to_file)
self.assertEqual('Document.docx', doc.frameset.child_framesets[1].frame_default_url)
self.assertFalse(doc.frameset.child_framesets[1].is_frame_link_to_file)
# Change properties for one of our frames.
doc.frameset.child_framesets[0].child_framesets[0].frame_default_url = 'https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx'
doc.frameset.child_framesets[0].child_framesets[0].is_frame_link_to_file = False
```

### See Also

* module [aspose.words.framesets](../../)
* class [FramesetCollection](../)

