---
title: DocumentBuilder.insert_ole_object method
linktitle: insert_ole_object method
articleTitle: insert_ole_object method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_ole_object method"
type: docs
weight: 420
url: /ru/python-net/aspose.words/documentbuilder/insert_ole_object/
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
# Вставьте таблицу Microsoft Excel из локальной файловой системы
# в документ, сохраняя её стандартный вид.
with system_helper.io.File.open(MY_DIR + 'Spreadsheet.xlsx', system_helper.io.FileMode.OPEN) as spreadsheet_stream:
    builder.writeln('Spreadsheet Ole object:')
    # Если параметр 'presentation' опущен и установлен 'asIcon', этот перегруженный метод выбирает
    # значок в соответствии с 'progId' и использует предопределённую подпись значка.
    builder.insert_ole_object(stream=spreadsheet_stream, prog_id='OleObject.xlsx', as_icon=False, presentation=None)
# Вставьте презентацию Microsoft Powerpoint в виде OLE‑объекта.
# На этот раз у неё будет изображение, загруженное из интернета, в качестве значка.
with system_helper.io.File.open(MY_DIR + 'Presentation.pptx', system_helper.io.FileMode.OPEN) as powerpoint_stream:
    img_bytes = system_helper.io.File.read_all_bytes(IMAGE_DIR + 'Logo.jpg')
    with io.BytesIO(img_bytes) as image_stream:
        builder.insert_paragraph()
        builder.writeln('Powerpoint Ole object:')
        builder.insert_ole_object(stream=powerpoint_stream, prog_id='OleObject.pptx', as_icon=True, presentation=image_stream)
# Дважды щёлкните эти объекты в Microsoft Word, чтобы открыть
# связанные файлы с помощью их соответствующих приложений.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObjects.docx')
```

Shows how to insert an OLE object into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# OLE‑объекты являются ссылками на файлы в нашей локальной файловой системе, которые могут быть открыты другими установленными приложениями.
# Двойной клик по этим фигурам запустит приложение, а затем использует его для открытия связанного объекта.
# Существует три способа использования метода InsertOleObject для вставки этих фигур и настройки их внешнего вида.
# 1 -  Изображение, взятое из локальной файловой системы:
with system_helper.io.FileStream(IMAGE_DIR + 'Logo.jpg', system_helper.io.FileMode.OPEN) as image_stream:
    # Если параметр 'presentation' опущен и установлен 'asIcon', этот перегруженный метод выбирает
    # значок в соответствии с расширением файла и использует имя файла в качестве подписи значка.
    builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', is_linked=False, as_icon=False, presentation=image_stream)
# Если параметр 'presentation' опущен и установлен 'asIcon', этот перегруженный метод выбирает
# значок в соответствии с 'progId' и использует имя файла в качестве подписи значка.
# 2 -  Значок, основанный на приложении, которое откроет объект:
builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', prog_id='Excel.Sheet', is_linked=False, as_icon=True, presentation=None)
# Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
# значок в соответствии с 'progId' и использует предопределённую подпись значка.
# 3 -  Значок‑изображение размером 32 × 32 пикселя или меньше из локальной файловой системы, с пользовательской подписью:
builder.insert_ole_object_as_icon(file_name=MY_DIR + 'Presentation.pptx', is_linked=False, icon_file=IMAGE_DIR + 'Logo icon.ico', icon_caption='Double click to view presentation!')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOleObject.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

