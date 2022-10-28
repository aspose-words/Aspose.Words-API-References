---
title: insert_ole_object method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.DocumentBuilder.insert_ole_object method"
type: docs
weight: 390
url: /python-net/aspose.words/documentbuilder/insert_ole_object/
---

## insert_ole_object(stream, prog_id, as_icon, presentation) {#bytesio_str_bool_bytesio}

Inserts an embedded OLE object from a stream into the document.


```python
def insert_ole_object(self, stream: BytesIO, prog_id: str, as_icon: bool, presentation: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |
| prog_id | str |  |
| as_icon | bool |  |
| presentation | BytesIO |  |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## insert_ole_object(file_name, is_linked, as_icon, presentation) {#str_bool_bool_bytesio}

Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using file extension.


```python
def insert_ole_object(self, file_name: str, is_linked: bool, as_icon: bool, presentation: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| is_linked | bool |  |
| as_icon | bool |  |
| presentation | BytesIO |  |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## insert_ole_object(file_name, prog_id, is_linked, as_icon, presentation) {#str_str_bool_bool_bytesio}

Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using given progID parameter.


```python
def insert_ole_object(self, file_name: str, prog_id: str, is_linked: bool, as_icon: bool, presentation: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| prog_id | str |  |
| is_linked | bool |  |
| as_icon | bool |  |
| presentation | BytesIO |  |

### Returns

Shape node containing Ole object and inserted at the current Builder position.


## Examples

Shows how to use document builder to embed OLE objects in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a Microsoft Excel spreadsheet from the local file system
# into the document while keeping its default appearance.
with open(MY_DIR + "Spreadsheet.xlsx", "rb") as spreadsheet_stream:

    builder.writeln("Spreadsheet Ole object:")
    # If 'presentation' is omitted and 'as_icon' is set, this overloaded method selects
    # the icon according to 'progId' and uses the predefined icon caption.
    builder.insert_ole_object(spreadsheet_stream, "OleObject.xlsx", False, None)

# Insert a Microsoft Powerpoint presentation as an OLE object.
# This time, it will have an image downloaded from the web for an icon.
with open(MY_DIR + "Presentation.pptx", "rb") as powerpoint_stream:

    with open(IMAGE_DIR + "Logo.jpg", "rb") as image_stream:
        builder.insert_paragraph()
        builder.writeln("Powerpoint Ole object:")
        builder.insert_ole_object(powerpoint_stream, "OleObject.pptx", True, image_stream)

# Double-click these objects in Microsoft Word to open
# the linked files using their respective applications.
doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_ole_objects.docx")
```

Shows how to insert an OLE object into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# OLE objects are links to files in our local file system that can be opened by other installed applications.
# Double clicking these shapes will launch the application, and then use it to open the linked object.
# There are three ways of using the "insert_ole_object" method to insert these shapes and configure their appearance.
# 1 -  Image taken from the local file system:
with open(IMAGE_DIR + "Logo.jpg", "rb") as image_stream:

    # If 'presentation' is omitted and 'as_icon' is set, this overloaded method selects
    # the icon according to the file extension and uses the filename for the icon caption.
    builder.insert_ole_object(MY_DIR + "Spreadsheet.xlsx", False, False, image_stream)

# If 'presentation' is omitted and 'as_icon' is set, this overloaded method selects
# the icon according to 'prog_id' and uses the filename for the icon caption.
# 2 -  Icon based on the application that will open the object:
builder.insert_ole_object(MY_DIR + "Spreadsheet.xlsx", "Excel.Sheet", False, True, None)

# If 'icon_file' and 'icon_caption' are omitted, this overloaded method selects
# the icon according to 'prog_id' and uses the predefined icon caption.
# 3 -  Image icon that's 32 x 32 pixels or smaller from the local file system, with a custom caption:
builder.insert_ole_object_as_icon(MY_DIR + "Presentation.pptx", False, IMAGE_DIR + "Logo icon.ico",
    "Double click to view presentation!")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_ole_object.docx")
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

