---
title: OlePackage class
linktitle: OlePackage class
articleTitle: OlePackage class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.OlePackage class. Allows to access OLE Package properties"
type: docs
weight: 260
url: /python-net/aspose.words.drawing/olepackage/
---

## OlePackage class

Allows to access OLE Package properties.
To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/python-net/working-with-ole-objects/) documentation article.




### Remarks

OLE package is a legacy and "undocumented" way to store embedded object if OLE handler is unknown.
Early Windows versions such as Windows 3.1, 95 and 98 had Packager.exe application which could be used to embed any type of data into document.
Now this application is excluded from Windows but MS Word and other applications still use it to embed data if OLE handler is missing or unknown.


### Properties

| Name | Description |
| --- | --- |
| [display_name](./display_name/) | Gets or sets OLE Package display name. |
| [file_name](./file_name/) | Gets or sets OLE Package file name. |

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

* module [aspose.words.drawing](../)

