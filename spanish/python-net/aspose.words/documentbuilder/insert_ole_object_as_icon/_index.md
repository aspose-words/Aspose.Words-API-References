---
title: DocumentBuilder.insert_ole_object_as_icon method
linktitle: insert_ole_object_as_icon method
articleTitle: insert_ole_object_as_icon method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_ole_object_as_icon method"
type: docs
weight: 430
url: /es/python-net/aspose.words/documentbuilder/insert_ole_object_as_icon/
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
# Los objetos OLE son enlaces a archivos en nuestro sistema de archivos local que pueden ser abiertos por otras aplicaciones instaladas.
# Al hacer doble clic en estas formas se lanzará la aplicación y luego se usará para abrir el objeto enlazado.
# Hay tres formas de usar el método InsertOleObject para insertar estas formas y configurar su apariencia.
# 1 -  Imagen tomada del sistema de archivos local:
with system_helper.io.FileStream(IMAGE_DIR + 'Logo.jpg', system_helper.io.FileMode.OPEN) as image_stream:
    # Si se omite 'presentation' y se establece 'asIcon', este método sobrecargado selecciona
    # el ícono según la extensión del archivo y usa el nombre del archivo como leyenda del ícono.
    builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', is_linked=False, as_icon=False, presentation=image_stream)
# Si se omite 'presentation' y se establece 'asIcon', este método sobrecargado selecciona
# el ícono según 'progId' y usa el nombre del archivo como leyenda del ícono.
# 2 -  Ícono basado en la aplicación que abrirá el objeto:
builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', prog_id='Excel.Sheet', is_linked=False, as_icon=True, presentation=None)
# Si se omiten 'iconFile' e 'iconCaption', este método sobrecargado selecciona
# el ícono según 'progId' y usa la leyenda de ícono predefinida.
# 3 -  Ícono de imagen de 32 x 32 píxeles o menos del sistema de archivos local, con una leyenda personalizada:
builder.insert_ole_object_as_icon(file_name=MY_DIR + 'Presentation.pptx', is_linked=False, icon_file=IMAGE_DIR + 'Logo icon.ico', icon_caption='Double click to view presentation!')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObject.docx')
```

Shows how to insert an embedded or linked OLE object as icon into the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Si se omiten 'iconFile' e 'iconCaption', este método sobrecargado selecciona
# el ícono según 'progId' y usa el nombre del archivo como leyenda del ícono.
builder.insert_ole_object_as_icon(file_name=MY_DIR + 'Presentation.pptx', prog_id='Package', is_linked=False, icon_file=IMAGE_DIR + 'Logo icon.ico', icon_caption='My embedded file')
builder.insert_break(aw.BreakType.LINE_BREAK)
with system_helper.io.FileStream(MY_DIR + 'Presentation.pptx', system_helper.io.FileMode.OPEN) as stream:
    # Si se omiten 'iconFile' e 'iconCaption', este método sobrecargado selecciona
    # el ícono según la extensión del archivo y usa el nombre del archivo como leyenda del ícono.
    shape = builder.insert_ole_object_as_icon(stream=stream, prog_id='PowerPoint.Application', icon_file=IMAGE_DIR + 'Logo icon.ico', icon_caption='My embedded file stream')
    set_ole_package = shape.ole_format.ole_package
    set_ole_package.file_name = 'Presentation.pptx'
    set_ole_package.display_name = 'Presentation.pptx'
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObjectAsIcon.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

