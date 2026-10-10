---
title: DocumentBuilder.insert_ole_object_as_icon method
linktitle: insert_ole_object_as_icon method
articleTitle: insert_ole_object_as_icon method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_ole_object_as_icon method"
type: docs
weight: 430
url: /zh/python-net/aspose.words/documentbuilder/insert_ole_object_as_icon/
---

## insert_ole_object_as_icon(file_name, is_linked, icon_file, icon_caption) {#str_bool_str_str}

Inserts an embedded or linked OLE object as icon into the document.
Allows to specify icon file and caption. Detects OLE object type using file extension.


```python
def insert_ole_object_as_icon(self, file_name: str, is_linked: bool, icon_file: str, icon_caption: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Full path to the file. |
| is_linked | bool | If ``True`` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| icon_file | str | Full path to the ICO file. If the value is ``None``, Aspose.Words will use a predefined image. |
| icon_caption | str | Icon caption. If the value is ``None``, Aspose.Words will use the file name. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## insert_ole_object_as_icon(file_name, prog_id, is_linked, icon_file, icon_caption) {#str_str_bool_str_str}

Inserts an embedded or linked OLE object as icon into the document.
Allows to specify icon file and caption. Detects OLE object type using given progID parameter.


```python
def insert_ole_object_as_icon(self, file_name: str, prog_id: str, is_linked: bool, icon_file: str, icon_caption: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Full path to the file. |
| prog_id | str | ProgId of OLE object. |
| is_linked | bool | If ``True`` then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| icon_file | str | Full path to the ICO file. If the value is ``None``, Aspose.Words will use a predefined image. |
| icon_caption | str | Icon caption. If the value is ``None``, Aspose.Words will use the file name. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## insert_ole_object_as_icon(stream, prog_id, icon_file, icon_caption) {#bytesio_str_str_str}

Inserts an embedded OLE object as icon from a stream into the document.
Allows to specify icon file and caption. Detects OLE object type using given progID parameter.


```python
def insert_ole_object_as_icon(self, stream: io.BytesIO, prog_id: str, icon_file: str, icon_caption: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Stream containing application data. |
| prog_id | str | ProgId of OLE object. |
| icon_file | str | Full path to the ICO file. If the value is ``None``, Aspose.Words will use a predefined image. |
| icon_caption | str | Icon caption. If the value is ``None``, Aspose.Words will use the a predefined icon caption. |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## Examples

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

Shows how to insert an embedded or linked OLE object as icon into the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 如果省略 'iconFile' 和 'iconCaption'，此重载方法将选择
# 根据 'progId' 选择图标，并使用文件名作为图标标题。
builder.insert_ole_object_as_icon(file_name=MY_DIR + 'Presentation.pptx', prog_id='Package', is_linked=False, icon_file=IMAGE_DIR + 'Logo icon.ico', icon_caption='My embedded file')
builder.insert_break(aw.BreakType.LINE_BREAK)
with system_helper.io.FileStream(MY_DIR + 'Presentation.pptx', system_helper.io.FileMode.OPEN) as stream:
    # 如果省略 'iconFile' 和 'iconCaption'，此重载方法将选择
    # 根据文件扩展名选择图标，并使用文件名作为图标标题。
    shape = builder.insert_ole_object_as_icon(stream=stream, prog_id='PowerPoint.Application', icon_file=IMAGE_DIR + 'Logo icon.ico', icon_caption='My embedded file stream')
    set_ole_package = shape.ole_format.ole_package
    set_ole_package.file_name = 'Presentation.pptx'
    set_ole_package.display_name = 'Presentation.pptx'
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObjectAsIcon.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

