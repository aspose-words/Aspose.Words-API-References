---
title: FieldOptions.custom_toc_style_separator property
linktitle: custom_toc_style_separator property
articleTitle: custom_toc_style_separator property
second_title: Aspose.Words for Python
description: "FieldOptions.custom_toc_style_separator property. Gets or sets custom style separator for the \\t switch in [FieldToc](../../fieldtoc/) field."
type: docs
weight: 60
url: /it/python-net/aspose.words.fields/fieldoptions/custom_toc_style_separator/
---

## FieldOptions.custom_toc_style_separator property

Gets or sets custom style separator for the \\t switch in [FieldToc](../../fieldtoc/) field.



```python
@property
def custom_toc_style_separator(self) -> str:
    ...

@custom_toc_style_separator.setter
def custom_toc_style_separator(self, value: str):
    ...

```

### Remarks

By default, custom styles defined by the \\t switch in the [FieldToc](../../fieldtoc/) field are separated by a delimiter taken from the current culture.
This property overrides that behaviour by specifying a user defined delimiter.



### Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
# Inserisci un campo TOC, che compilerà tutti i titoli in un indice.
# Per ogni titolo, questo campo creerà una riga con il testo di quello stile di titolo a sinistra,
# e la pagina su cui appare il titolo a destra.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Usa la proprietà BookmarkName per elencare solo i titoli
# che compaiono entro i limiti di un segnalibro con il nome "MyBookmark".
field.bookmark_name = 'MyBookmark'
# Il testo con uno stile di titolo incorporato, come "Heading 1", applicato a esso verrà considerato un titolo.
# Possiamo specificare stili aggiuntivi da riconoscere come titoli dal TOC in questa proprietà e i loro livelli TOC.
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# Per impostazione predefinita, gli stili/livelli TOC sono separati nella proprietà CustomStyles da una virgola,
# ma possiamo impostare un delimitatore personalizzato in questa proprietà.
doc.field_options.custom_toc_style_separator = ';'
# Configura il campo per escludere i titoli che hanno livelli TOC al di fuori di questo intervallo.
field.heading_level_range = '1-3'
# Il TOC non mostrerà i numeri di pagina dei titoli i cui livelli TOC sono entro questo intervallo.
field.page_number_omitting_level_range = '2-5'
# Imposta una stringa personalizzata che separerà ogni titolo dal suo numero di pagina.
field.entry_separator = '-'
field.insert_hyperlinks = True
field.hide_in_web_layout = False
field.preserve_line_breaks = True
field.preserve_tabs = True
field.use_paragraph_outline_level = False
self.insert_new_page_with_heading(builder, 'First entry', 'Heading 1')
builder.writeln('Paragraph text.')
self.insert_new_page_with_heading(builder, 'Second entry', 'Heading 1')
self.insert_new_page_with_heading(builder, 'Third entry', 'Quote')
self.insert_new_page_with_heading(builder, 'Fourth entry', 'Intense Quote')
# Questi due titoli avranno i numeri di pagina omessi perché sono entro l'intervallo "2-5".
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# Questa voce non appare perché "Heading 4" è al di fuori dell'intervallo "1-3" che abbiamo impostato in precedenza.
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# Questa voce non appare perché è al di fuori del segnalibro specificato dal sommario.
self.insert_new_page_with_heading(builder, 'Eighth entry', 'Heading 1')
self.assertEqual(' TOC  \\b MyBookmark \\t "Quote; 6; Intense Quote; 7" \\o 1-3 \\n 2-5 \\p - \\h \\u0000 \\w', field.get_field_code())
field.update_page_numbers()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.docx')
```

Shows how to insert a TOC, and populate it with entries based on heading styles (InsertNewPageWithHeading).

```python
def insert_new_page_with_heading(self, builder, caption_text, style_name):
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    original_style = builder.paragraph_format.style_name
    builder.paragraph_format.style = builder.document.styles.get_by_name(style_name)
    builder.writeln(caption_text)
    builder.paragraph_format.style = builder.document.styles.get_by_name(original_style)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

