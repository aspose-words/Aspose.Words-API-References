---
title: OleFormat.ole_package property
linktitle: ole_package property
articleTitle: ole_package property
second_title: Aspose.Words for Python
description: "OleFormat.ole_package property. Provide access to [OlePackage](../../olepackage/) if OLE object is an OLE Package"
type: docs
weight: 80
url: /python-net/aspose.words.drawing/oleformat/ole_package/
---

## OleFormat.ole_package property

Provide access to [OlePackage](../../olepackage/) if OLE object is an OLE Package.
Returns ``None`` otherwise.



```python
@property
def ole_package(self) -> aspose.words.drawing.OlePackage:
    ...

```

### Remarks

OLE Package is a legacy technology that allows to wrap any file format not present in the OLE registry of
a Windows system into a generic package allowing to embed almost anything into a document.
See [OlePackage](../../olepackage/) type for more info.



### Examples

Shows how insert an OLE object into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# OLE objects allow us to open other files in the local file system using another installed application
# in our operating system by double-clicking on the shape that contains the OLE object in the document body.
# In this case, our external file will be a ZIP archive.
zip_file_bytes = system_helper.io.File.read_all_bytes(DATABASE_DIR + 'cat001.zip')
with io.BytesIO(zip_file_bytes) as stream:
    shape = builder.insert_ole_object(stream=stream, prog_id='Package', as_icon=True, presentation=None)
    shape.ole_format.ole_package.file_name = 'Package file name.zip'
    shape.ole_format.ole_package.display_name = 'Package display name.zip'
doc.save(file_name=ARTIFACTS_DIR + 'Shape.InsertOlePackage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

