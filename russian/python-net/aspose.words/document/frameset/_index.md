---
title: Document.frameset property
linktitle: frameset property
articleTitle: frameset property
second_title: Aspose.Words for Python
description: "Document.frameset property. Returns a [Document.frameset](./) instance if this document represents a frames page."
type: docs
weight: 170
url: /ru/python-net/aspose.words/document/frameset/
---

## Document.frameset property

Returns a [Document.frameset](./) instance if this document represents a frames page.



```python
@property
def frameset(self) -> aspose.words.framesets.Frameset:
    ...

```

### Remarks

If the document is not framed, the property has the ``None`` value.



### Examples

Shows how to access frames on-page.

```python
# Документ содержит несколько фреймов со ссылками на другие документы.
doc = aw.Document(file_name=MY_DIR + 'Frameset.docx')
self.assertEqual(3, doc.frameset.child_framesets.count)
# Мы можем проверить URL по умолчанию (URL веб‑страницы или локального документа) или то, является ли фрейм внешним ресурсом.
self.assertEqual('https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx', doc.frameset.child_framesets[0].child_framesets[0].frame_default_url)
self.assertTrue(doc.frameset.child_framesets[0].child_framesets[0].is_frame_link_to_file)
self.assertEqual('Document.docx', doc.frameset.child_framesets[1].frame_default_url)
self.assertFalse(doc.frameset.child_framesets[1].is_frame_link_to_file)
# Измените свойства одного из наших фреймов.
doc.frameset.child_framesets[0].child_framesets[0].frame_default_url = 'https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx'
doc.frameset.child_framesets[0].child_framesets[0].is_frame_link_to_file = False
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

