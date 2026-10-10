---
title: FieldToc class
linktitle: FieldToc class
articleTitle: FieldToc class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldToc class. Implements the TOC field"
type: docs
weight: 1070
url: /de/python-net/aspose.words.fields/fieldtoc/
---

## FieldToc class

Implements the TOC field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Builds a table of contents (which can also be a table of figures) using the entries specified by TC fields,
their heading levels, and specified styles, and inserts that table at this place in the document.


**Inheritance:** [FieldToc](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldToc()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [captionless_table_of_figures_label](./captionless_table_of_figures_label/) | Gets or sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [custom_styles](./custom_styles/) | Gets or sets a list of styles other than the built-in heading styles to include in the table of contents. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_identifier](./entry_identifier/) | Gets or sets a string that should match type identifiers of TC fields being included. |
| [entry_level_range](./entry_level_range/) | Gets or sets a range of levels of the table of contents entries to be included. |
| [entry_separator](./entry_separator/) | Gets or sets a sequence of characters that separate an entry and its page number. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [heading_level_range](./heading_level_range/) | Gets or sets a range of heading levels to include. |
| [hide_in_web_layout](./hide_in_web_layout/) | Gets or sets whether to hide tab leader and page numbers in Web layout view. |
| [insert_hyperlinks](./insert_hyperlinks/) | Gets or sets whether to make the table of contents entries hyperlinks. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [page_number_omitting_level_range](./page_number_omitting_level_range/) | Gets or sets a range of levels of the table of contents entries from which to omits page numbers. |
| [prefixed_sequence_identifier](./prefixed_sequence_identifier/) | Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number. |
| [preserve_line_breaks](./preserve_line_breaks/) | Gets or sets whether to preserve newline characters within table entries. |
| [preserve_tabs](./preserve_tabs/) | Gets or sets whether to preserve tab entries within table entries. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_separator](./sequence_separator/) | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [table_of_figures_label](./table_of_figures_label/) | Gets or sets the name of the sequence identifier used when building a table of figures. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [use_paragraph_outline_level](./use_paragraph_outline_level/) | Gets or sets whether to use the applied paragraph outline level. |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update_page_numbers()](./update_page_numbers/#default) | Updates the page numbers for items in this table of contents. |

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

Shows how to populate a TOC field with entries using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag in seinem Inhaltsverzeichnis erstellen.
# Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält, sowie die Seitennummer, auf der das Feld erscheint.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
# Diese Felder führen außerdem separate Zählungen für jede eindeutig benannte Sequenz.
# identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
# Verwenden Sie die "TableOfFiguresLabel"-Eigenschaft, um eine Hauptsequenz für das TOC zu benennen.
# Jetzt wird dieses TOC nur Einträge aus SEQ-Feldern erstellen, deren "SequenceIdentifier" auf "MySequence" gesetzt ist.
field_toc.table_of_figures_label = 'MySequence'
# Wir können eine weitere SEQ-Feldsequenz in der "PrefixedSequenceIdentifier"-Eigenschaft benennen.
# SEQ-Felder aus dieser Präfixsequenz werden keine TOC-Einträge erzeugen.
# Jeder aus einem Hauptsequenz-SEQ-Feld erstellte TOC-Eintrag wird nun ebenfalls die Zählung anzeigen, die
# Die Präfixsequenz befindet sich derzeit im primären Sequenz‑SEQ‑Feld, das den Eintrag erzeugt hat.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Jeder TOC‑Eintrag zeigt die Präfixsequenz‑Zählung sofort links davon an
# der Seitenzahl, auf der das Hauptsequenz‑SEQ‑Feld erscheint.
# Wir können einen benutzerdefinierten Trennzeichen angeben, das zwischen diesen beiden Zahlen erscheint.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Es gibt zwei Möglichkeiten, SEQ‑Felder zu verwenden, um dieses TOC zu füllen.
# 1 -  Einfügen eines SEQ‑Feldes, das zur Präfixsequenz des TOC gehört:
# Dieses Feld erhöht die SEQ‑Sequenz‑Zählung für "PrefixSequence" um 1.
# Da dieses Feld nicht zur identifizierten Hauptsequenz gehört
# durch die "TableOfFiguresLabel"‑Eigenschaft des TOC, wird es nicht als Eintrag erscheinen.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 -  Einfügen eines SEQ‑Feldes, das zur Hauptsequenz des TOC gehört:
# Dieses SEQ‑Feld wird einen Eintrag im TOC erzeugen.
# Der TOC‑Eintrag enthält den Absatz, in dem das SEQ‑Feld steht, sowie die Seitenzahl, auf der es erscheint.
# Dieser Eintrag zeigt außerdem die aktuelle Zählung der Präfixsequenz an,
# getrennt von der Seitenzahl durch den Wert in der "SeqenceSeparator"‑Eigenschaft des TOC.
# Die Zählung von "PrefixSequence" ist 1, dieses Hauptsequenz‑SEQ‑Feld befindet sich auf Seite 2,
# und das Trennzeichen ist ">", sodass der Eintrag "1>2" anzeigt.
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Fügen Sie eine Seite ein, erhöhen Sie die Präfixsequenz um 2 und fügen Sie anschließend ein SEQ‑Feld ein, um einen TOC‑Eintrag zu erstellen.
# Die Präfixsequenz ist jetzt 2, und das Hauptsequenz‑SEQ‑Feld befindet sich auf Seite 3,
# so zeigt der TOC‑Eintrag "2>3" bei seiner Seitenzahl an.
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
builder.write('Second TOC entry, MySequence #')
field_seq.sequence_identifier = 'MySequence'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.SEQ.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

