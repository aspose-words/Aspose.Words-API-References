---
title: Frameset.child_framesets property
linktitle: child_framesets property
articleTitle: child_framesets property
second_title: Aspose.Words for Python
description: "Frameset.child_framesets property. Gets the collection of child frames and frames pages."
type: docs
weight: 20
url: /es/python-net/aspose.words.framesets/frameset/child_framesets/
---

## Frameset.child_framesets property

Gets the collection of child frames and frames pages.


```python
@property
def child_framesets(self) -> aspose.words.framesets.FramesetCollection:
    ...

```

### Examples

Shows how to access frames on-page.

```python
# El documento contiene varios marcos con enlaces a otros documentos.
doc = aw.Document(file_name=MY_DIR + 'Frameset.docx')
self.assertEqual(3, doc.frameset.child_framesets.count)
# Podemos comprobar la URL predeterminada (una URL de página web o documento local) o si el marco es un recurso externo.
self.assertEqual('https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx', doc.frameset.child_framesets[0].child_framesets[0].frame_default_url)
self.assertTrue(doc.frameset.child_framesets[0].child_framesets[0].is_frame_link_to_file)
self.assertEqual('Document.docx', doc.frameset.child_framesets[1].frame_default_url)
self.assertFalse(doc.frameset.child_framesets[1].is_frame_link_to_file)
# Cambie las propiedades de uno de nuestros marcos.
doc.frameset.child_framesets[0].child_framesets[0].frame_default_url = 'https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx'
doc.frameset.child_framesets[0].child_framesets[0].is_frame_link_to_file = False
```

### See Also

* module [aspose.words.framesets](../../)
* class [Frameset](../)

