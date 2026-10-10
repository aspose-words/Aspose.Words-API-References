---
title: OlePackage.display_name property
linktitle: display_name property
articleTitle: display_name property
second_title: Aspose.Words for Python
description: "OlePackage.display_name property. Gets or sets OLE Package display name."
type: docs
weight: 10
url: /zh/python-net/aspose.words.drawing/olepackage/display_name/
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
# OLE 对象允许我们使用另一个已安装的应用程序打开本地文件系统中的其他文件
# 通过在文档主体中双击包含 OLE 对象的形状，在我们的操作系统中使用已安装的其他应用程序打开文件。
# 在这种情况下，我们的外部文件将是 ZIP 压缩包。
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

