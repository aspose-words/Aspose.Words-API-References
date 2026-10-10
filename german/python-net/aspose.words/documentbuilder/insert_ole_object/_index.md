---
title: DocumentBuilder.insert_ole_object method
linktitle: insert_ole_object method
articleTitle: insert_ole_object method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_ole_object method"
type: docs
weight: 420
url: /de/python-net/aspose.words/documentbuilder/insert_ole_object/
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
# Fügen Sie eine Microsoft Excel‑Tabelle aus dem lokalen Dateisystem ein
# in das Dokument ein, wobei das Standardaussehen beibehalten wird.
with system_helper.io.File.open(MY_DIR + 'Spreadsheet.xlsx', system_helper.io.FileMode.OPEN) as spreadsheet_stream:
    builder.writeln('Spreadsheet Ole object:')
    # Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode
    # das Symbol basierend auf 'progId' aus und verwendet die vordefinierte Symbolbeschriftung.
    builder.insert_ole_object(stream=spreadsheet_stream, prog_id='OleObject.xlsx', as_icon=False, presentation=None)
# Fügen Sie eine Microsoft Powerpoint‑Präsentation als OLE‑Objekt ein.
# Dieses Mal wird es ein aus dem Web heruntergeladenes Bild als Symbol haben.
with system_helper.io.File.open(MY_DIR + 'Presentation.pptx', system_helper.io.FileMode.OPEN) as powerpoint_stream:
    img_bytes = system_helper.io.File.read_all_bytes(IMAGE_DIR + 'Logo.jpg')
    with io.BytesIO(img_bytes) as image_stream:
        builder.insert_paragraph()
        builder.writeln('Powerpoint Ole object:')
        builder.insert_ole_object(stream=powerpoint_stream, prog_id='OleObject.pptx', as_icon=True, presentation=image_stream)
# Doppelklicken Sie diese Objekte in Microsoft Word, um zu öffnen
# die verknüpften Dateien mit ihren jeweiligen Anwendungen.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObjects.docx')
```

Shows how to insert an OLE object into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# OLE-Objekte sind Verknüpfungen zu Dateien in unserem lokalen Dateisystem, die von anderen installierten Anwendungen geöffnet werden können.
# Durch Doppelklicken auf diese Formen wird die Anwendung gestartet und anschließend zum Öffnen des verknüpften Objekts verwendet.
# Es gibt drei Möglichkeiten, die InsertOleObject-Methode zu verwenden, um diese Formen einzufügen und ihr Aussehen zu konfigurieren.
# 1 -  Bild aus dem lokalen Dateisystem:
with system_helper.io.FileStream(IMAGE_DIR + 'Logo.jpg', system_helper.io.FileMode.OPEN) as image_stream:
    # Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode
    # das Symbol basierend auf der Dateierweiterung aus und verwendet den Dateinamen für die Symbolbeschriftung.
    builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', is_linked=False, as_icon=False, presentation=image_stream)
# Wenn 'presentation' weggelassen wird und 'asIcon' gesetzt ist, wählt diese überladene Methode
# das Symbol basierend auf 'progId' aus und verwendet den Dateinamen für die Symbolbeschriftung.
# 2 -  Symbol basierend auf der Anwendung, die das Objekt öffnen wird:
builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', prog_id='Excel.Sheet', is_linked=False, as_icon=True, presentation=None)
# Wenn 'iconFile' und 'iconCaption' weggelassen werden, wählt diese überladene Methode
# das Symbol basierend auf 'progId' aus und verwendet die vordefinierte Symbolbeschriftung.
# 3 -  Bildsymbol, das 32 x 32 Pixel oder kleiner ist, aus dem lokalen Dateisystem, mit einer benutzerdefinierten Beschriftung:
builder.insert_ole_object_as_icon(file_name=MY_DIR + 'Presentation.pptx', is_linked=False, icon_file=IMAGE_DIR + 'Logo icon.ico', icon_caption='Double click to view presentation!')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObject.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

