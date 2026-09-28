---
title: OlePackage.display_name property
linktitle: display_name property
articleTitle: display_name property
second_title: Aspose.Words for Python
description: "OlePackage.display_name property. Gets or sets OLE Package display name."
type: docs
weight: 10
url: /fr/python-net/aspose.words.drawing/olepackage/display_name/
---

## OlePackage.display_name property

Gets or sets OLE Package display name.


```python
@property
def display_name(self) -> str:
    ...

@display_name.setter
def display_name(self, value: str):
    ...

```

### Examples

Shows how insert an OLE object into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Les objets OLE nous permettent d'ouvrir d'autres fichiers du système de fichiers local en utilisant une autre application installée
# dans notre système d'exploitation en double-cliquant sur la forme qui contient l'objet OLE dans le corps du document.
# Dans ce cas, notre fichier externe sera une archive ZIP.
zip_file_bytes = system_helper.io.File.read_all_bytes(DATABASE_DIR + 'cat001.zip')
with io.BytesIO(zip_file_bytes) as stream:
    shape = builder.insert_ole_object(stream=stream, prog_id='Package', as_icon=True, presentation=None)
    shape.ole_format.ole_package.file_name = 'Package file name.zip'
    shape.ole_format.ole_package.display_name = 'Package display name.zip'
doc.save(file_name=ARTIFACTS_DIR + 'Shape.InsertOlePackage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [OlePackage](../)

