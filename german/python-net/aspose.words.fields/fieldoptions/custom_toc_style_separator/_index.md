---
title: FieldOptions.custom_toc_style_separator property
linktitle: custom_toc_style_separator property
articleTitle: custom_toc_style_separator property
second_title: Aspose.Words for Python
description: "FieldOptions.custom_toc_style_separator property. Gets or sets custom style separator for the \\t switch in [FieldToc](../../fieldtoc/) field."
type: docs
weight: 60
url: /de/python-net/aspose.words.fields/fieldoptions/custom_toc_style_separator/
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
# Fügen Sie ein TOC-Feld ein, das alle Überschriften zu einem Inhaltsverzeichnis zusammenstellt.
# Für jede Überschrift erzeugt dieses Feld eine Zeile mit dem Text im jeweiligen Überschriftsstil links,
# und die Seite, auf der die Überschrift erscheint, rechts.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Verwenden Sie die BookmarkName-Eigenschaft, um nur Überschriften aufzulisten
# die innerhalb der Grenzen eines Lesezeichens mit dem Namen "MyBookmark" erscheinen.
field.bookmark_name = 'MyBookmark'
# Text mit einem integrierten Überschriftsstil, wie "Heading 1", wird als Überschrift gezählt.
# Wir können zusätzliche Stile benennen, die vom TOC in dieser Eigenschaft als Überschriften erkannt werden, sowie deren TOC‑Ebenen.
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# Standardmäßig werden Stile/TOC‑Ebenen in der CustomStyles‑Eigenschaft durch ein Komma getrennt,
# aber wir können in dieser Eigenschaft ein benutzerdefiniertes Trennzeichen festlegen.
doc.field_options.custom_toc_style_separator = ';'
# Konfigurieren Sie das Feld, um alle Überschriften auszuschließen, deren TOC‑Ebenen außerhalb dieses Bereichs liegen.
field.heading_level_range = '1-3'
# Das TOC zeigt die Seitenzahlen von Überschriften, deren TOC‑Ebenen innerhalb dieses Bereichs liegen, nicht an.
field.page_number_omitting_level_range = '2-5'
# Legen Sie eine benutzerdefinierte Zeichenkette fest, die jede Überschrift von ihrer Seitenzahl trennt.
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
# Diese beiden Überschriften erhalten keine Seitenzahlen, weil sie im Bereich "2-5" liegen.
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# Dieser Eintrag erscheint nicht, weil "Heading 4" außerhalb des zuvor festgelegten Bereichs "1-3" liegt.
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# Dieser Eintrag wird nicht angezeigt, weil er außerhalb des vom Inhaltsverzeichnis angegebenen Lesezeichens liegt.
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

