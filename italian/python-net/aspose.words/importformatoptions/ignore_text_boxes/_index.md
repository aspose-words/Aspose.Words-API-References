---
title: ImportFormatOptions.ignore_text_boxes property
linktitle: ignore_text_boxes property
articleTitle: ignore_text_boxes property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.ignore_text_boxes property. Gets or sets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode is used"
type: docs
weight: 60
url: /it/python-net/aspose.words/importformatoptions/ignore_text_boxes/
---

## ImportFormatOptions.ignore_text_boxes property

Gets or sets a boolean value that specifies that source formatting of textboxes content ignored
if [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode is used.
The default value is ``True``.



```python
@property
def ignore_text_boxes(self) -> bool:
    ...

@ignore_text_boxes.setter
def ignore_text_boxes(self, value: bool):
    ...

```

### Examples

Shows how to manage text box formatting while appending a document.

```python
# Crea un documento in cui verranno inseriti i nodi di un altro documento.
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=dst_doc)
builder.writeln('Hello world!')
# Crea un altro documento con una casella di testo, che importeremo nel primo documento.
src_doc = aw.Document()
builder = aw.DocumentBuilder(doc=src_doc)
text_box = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=300, height=100)
builder.move_to(text_box.first_paragraph)
builder.paragraph_format.style.font.name = 'Courier New'
builder.paragraph_format.style.font.size = 24
builder.write('Textbox contents')
# Imposta un flag per specificare se cancellare o preservare la formattazione della casella di testo
# durante l'importazione in altri documenti.
import_format_options = aw.ImportFormatOptions()
import_format_options.ignore_text_boxes = ignore_text_boxes
# Importa la casella di testo dal documento di origine nel documento di destinazione,
# e poi verifica se abbiamo preservato lo stile del suo contenuto testuale.
importer = aw.NodeImporter(src_doc=src_doc, dst_doc=dst_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=import_format_options)
imported_text_box = importer.import_node(text_box, True).as_shape()
dst_doc.first_section.body.paragraphs[1].append_child(imported_text_box)
if ignore_text_boxes:
    self.assertEqual(12, imported_text_box.first_paragraph.runs[0].font.size)
    self.assertEqual('Times New Roman', imported_text_box.first_paragraph.runs[0].font.name)
else:
    self.assertEqual(24, imported_text_box.first_paragraph.runs[0].font.size)
    self.assertEqual('Courier New', imported_text_box.first_paragraph.runs[0].font.name)
dst_doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.IgnoreTextBoxes.docx')
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

