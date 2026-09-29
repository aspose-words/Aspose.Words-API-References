---
title: DocumentBuilder.insert_ole_object method
linktitle: insert_ole_object method
articleTitle: insert_ole_object method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_ole_object method"
type: docs
weight: 420
url: /sv/python-net/aspose.words/documentbuilder/insert_ole_object/
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
# Infoga ett Microsoft Excel-kalkylblad från det lokala filsystemet
# i dokumentet samtidigt som dess standardutseende behålls.
with system_helper.io.File.open(MY_DIR + 'Spreadsheet.xlsx', system_helper.io.FileMode.OPEN) as spreadsheet_stream:
    builder.writeln('Spreadsheet Ole object:')
    # Om 'presentation' utelämnas och 'asIcon' är satt, väljer denna överlagrade metod
    # ikonen enligt 'progId' och använder den fördefinierade ikonrubriken.
    builder.insert_ole_object(stream=spreadsheet_stream, prog_id='OleObject.xlsx', as_icon=False, presentation=None)
# Infoga en Microsoft Powerpoint-presentation som ett OLE-objekt.
# Den här gången kommer den att ha en bild hämtad från webben som en ikon.
with system_helper.io.File.open(MY_DIR + 'Presentation.pptx', system_helper.io.FileMode.OPEN) as powerpoint_stream:
    img_bytes = system_helper.io.File.read_all_bytes(IMAGE_DIR + 'Logo.jpg')
    with io.BytesIO(img_bytes) as image_stream:
        builder.insert_paragraph()
        builder.writeln('Powerpoint Ole object:')
        builder.insert_ole_object(stream=powerpoint_stream, prog_id='OleObject.pptx', as_icon=True, presentation=image_stream)
# Dubbelklicka på dessa objekt i Microsoft Word för att öppna
# de länkade filerna med deras respektive program.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObjects.docx')
```

Shows how to insert an OLE object into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# OLE-objekt är länkar till filer i vårt lokala filsystem som kan öppnas av andra installerade program.
# Att dubbelklicka på dessa former startar programmet och använder det sedan för att öppna det länkade objektet.
# Det finns tre sätt att använda metoden InsertOleObject för att infoga dessa former och konfigurera deras utseende.
# 1 -  Bild hämtad från det lokala filsystemet:
with system_helper.io.FileStream(IMAGE_DIR + 'Logo.jpg', system_helper.io.FileMode.OPEN) as image_stream:
    # Om 'presentation' utelämnas och 'asIcon' är satt, väljer denna överlagrade metod
    # ikonen enligt filändelsen och använder filnamnet för ikonens rubrik.
    builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', is_linked=False, as_icon=False, presentation=image_stream)
# Om 'presentation' utelämnas och 'asIcon' är satt, väljer denna överlagrade metod
# ikonen enligt 'progId' och använder filnamnet för ikonens rubrik.
# 2 -  Ikon baserad på programmet som kommer att öppna objektet:
builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', prog_id='Excel.Sheet', is_linked=False, as_icon=True, presentation=None)
# Om 'iconFile' och 'iconCaption' utelämnas, väljer denna överlagrade metod
# ikonen enligt 'progId' och använder den fördefinierade ikonrubriken.
# 3 -  Bildikon som är 32 x 32 pixlar eller mindre från det lokala filsystemet, med en anpassad rubrik:
builder.insert_ole_object_as_icon(file_name=MY_DIR + 'Presentation.pptx', is_linked=False, icon_file=IMAGE_DIR + 'Logo icon.ico', icon_caption='Double click to view presentation!')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObject.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

