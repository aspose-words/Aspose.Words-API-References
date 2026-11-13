---
title: Frameset.frame_default_url property
linktitle: frame_default_url property
articleTitle: frame_default_url property
second_title: Aspose.Words for Python
description: "Frameset.frame_default_url property. Gets or sets the web page URL or document file name to display in this frame."
type: docs
weight: 30
url: /es/python-net/aspose.words.framesets/frameset/frame_default_url/
---

## Frameset.frame_default_url property

Gets or sets the web page URL or document file name to display in this frame.


```python
@property
def frame_default_url(self) -> str:
    ...

@frame_default_url.setter
def frame_default_url(self, value: str):
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

