---
title: frameset property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns a [Document.frameset](./) instance if this document represents a frames page."
type: docs
weight: 160
url: /python-net/aspose.words/document/frameset/
---

## Document.frameset property

Returns a [Document.frameset](./) instance if this document represents a frames page.


If the document is not framed, the property has the ``None`` value.



### Examples

Shows how to access frames on-page.

```python
# Document contains several frames with links to other documents.
doc = aw.Document(MY_DIR + "Frameset.docx")

# We can check the default URL (a web page URL or local document) or if the frame is an external resource.
self.assertEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.frameset.child_framesets[0].child_framesets[0].frame_default_url)
self.assertTrue(doc.frameset.child_framesets[0].child_framesets[0].is_frame_link_to_file)

self.assertEqual("Document.docx", doc.frameset.child_framesets[1].frame_default_url)
self.assertFalse(doc.frameset.child_framesets[1].is_frame_link_to_file)

# Change properties for one of our frames.
doc.frameset.child_framesets[0].child_framesets[0].frame_default_url = "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx"
doc.frameset.child_framesets[0].child_framesets[0].is_frame_link_to_file = False
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

