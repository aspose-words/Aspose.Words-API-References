---
title: DocumentBuilder.insert_ole_object method
linktitle: insert_ole_object method
articleTitle: insert_ole_object method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_ole_object method"
type: docs
weight: 420
url: /zh/python-net/aspose.words/documentbuilder/insert_ole_object/
---

## insert_ole_object(stream, prog_id, as_icon, presentation) {#bytesio_str_bool_bytesio}

Inserts an embedded OLE object from a stream into the document.


```python
def insert_ole_object(self, stream: io.BytesIO, prog_id: str, as_icon: bool, presentation: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Stream containing application data. |
| prog_id | str | Programmatic Identifier of OLE object. |
| as_icon | bool | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | io.BytesIO | Image presentation of OLE object. If value is ``None`` Aspose.Words will use one of the predefined images. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## insert_ole_object(file_name, is_linked, as_icon, presentation) {#str_bool_bool_bytesio}

Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using file extension.


```python
def insert_ole_object(self, file_name: str, is_linked: bool, as_icon: bool, presentation: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Full path to the file. |
| is_linked | bool | If ``True`` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| as_icon | bool | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | io.BytesIO | Image presentation of OLE object. If value is ``None`` Aspose.Words will use one of the predefined images. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## insert_ole_object(file_name, prog_id, is_linked, as_icon, presentation) {#str_str_bool_bool_bytesio}

Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using given progID parameter.


```python
def insert_ole_object(self, file_name: str, prog_id: str, is_linked: bool, as_icon: bool, presentation: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Full path to the file. |
| prog_id | str | ProgId of OLE object. |
| is_linked | bool | If ``True`` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| as_icon | bool | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | io.BytesIO | Image presentation of OLE object. If value is ``None`` Aspose.Words will use one of the predefined images. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## Examples

Shows how to use document builder to embed OLE objects in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 从本地文件系统插入 Microsoft Excel 电子表格
# 将其插入文档，同时保持默认外观。
with system_helper.io.File.open(MY_DIR + 'Spreadsheet.xlsx', system_helper.io.FileMode.OPEN) as spreadsheet_stream:
    builder.writeln('Spreadsheet Ole object:')
    # 如果省略 'presentation' 并设置了 'asIcon'，此重载方法将选择
    # 根据 'progId' 选择图标，并使用预定义的图标标题。
    builder.insert_ole_object(stream=spreadsheet_stream, prog_id='OleObject.xlsx', as_icon=False, presentation=None)
# 将 Microsoft Powerpoint 演示文稿插入为 OLE 对象。
# 这次，它将使用从网络下载的图像作为图标。
with system_helper.io.File.open(MY_DIR + 'Presentation.pptx', system_helper.io.FileMode.OPEN) as powerpoint_stream:
    img_bytes = system_helper.io.File.read_all_bytes(IMAGE_DIR + 'Logo.jpg')
    with io.BytesIO(img_bytes) as image_stream:
        builder.insert_paragraph()
        builder.writeln('Powerpoint Ole object:')
        builder.insert_ole_object(stream=powerpoint_stream, prog_id='OleObject.pptx', as_icon=True, presentation=image_stream)
# 在 Microsoft Word 中双击这些对象以打开
# 使用各自的应用程序打开链接的文件。
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObjects.docx')
```

Shows how to insert an OLE object into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# OLE 对象是指向本地文件系统中文件的链接，可由其他已安装的应用程序打开。
# 双击这些形状将启动相应的应用程序，然后使用它打开链接的对象。
# 使用 InsertOleObject 方法插入这些形状并配置其外观有三种方式。
# 1 -  从本地文件系统获取的图像：
with system_helper.io.FileStream(IMAGE_DIR + 'Logo.jpg', system_helper.io.FileMode.OPEN) as image_stream:
    # 如果省略 'presentation' 并设置了 'asIcon'，此重载方法将选择
    # 根据文件扩展名选择图标，并使用文件名作为图标标题。
    builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', is_linked=False, as_icon=False, presentation=image_stream)
# 如果省略 'presentation' 并设置了 'asIcon'，此重载方法将选择
# 根据 'progId' 选择图标，并使用文件名作为图标标题。
# 2 -  基于将打开对象的应用程序的图标：
builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', prog_id='Excel.Sheet', is_linked=False, as_icon=True, presentation=None)
# 如果省略 'iconFile' 和 'iconCaption'，此重载方法将选择
# 根据 'progId' 选择图标，并使用预定义的图标标题。
# 3 -  来自本地文件系统的 32 x 32 像素或更小的图像图标，带自定义标题：
builder.insert_ole_object_as_icon(file_name=MY_DIR + 'Presentation.pptx', is_linked=False, icon_file=IMAGE_DIR + 'Logo icon.ico', icon_caption='Double click to view presentation!')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObject.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

