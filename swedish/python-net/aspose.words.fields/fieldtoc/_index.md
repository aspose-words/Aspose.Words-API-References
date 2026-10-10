---
title: FieldToc class
linktitle: FieldToc class
articleTitle: FieldToc class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldToc class. Implements the TOC field"
type: docs
weight: 1070
url: /sv/python-net/aspose.words.fields/fieldtoc/
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
# Infoga ett TOC-fält, som kommer att samla alla rubriker i en innehållsförteckning.
# För varje rubrik kommer detta fält att skapa en rad med texten i den rubrikstilen till vänster,
# och sidan där rubriken visas till höger.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Använd egenskapen BookmarkName för att endast lista rubriker
# som visas inom gränserna för ett bokmärke med namnet \"MyBookmark\".
field.bookmark_name = 'MyBookmark'
# Text med en inbyggd rubrikstil, såsom \"Heading 1\", som tillämpas på den räknas som en rubrik.
# Vi kan namnge ytterligare stilar som ska plockas upp som rubriker av TOC i den här egenskapen och deras TOC-nivåer.
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# Som standard separeras Styles/TOC-nivåer i egenskapen CustomStyles med ett kommatecken,
# men vi kan ange en anpassad avgränsare i denna egenskap.
doc.field_options.custom_toc_style_separator = ';'
# Konfigurera fältet för att exkludera alla rubriker som har TOC-nivåer utanför detta intervall.
field.heading_level_range = '1-3'
# TOC kommer inte att visa sidnumren för rubriker vars TOC-nivåer ligger inom detta intervall.
field.page_number_omitting_level_range = '2-5'
# Ange en anpassad sträng som separerar varje rubrik från dess sidnummer.
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
# Dessa två rubriker kommer att ha sidnumren utelämnade eftersom de ligger inom intervallet \"2-5\".
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# Denna post visas inte eftersom \"Heading 4\" ligger utanför intervallet \"1-3\" som vi tidigare har angett.
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# Den här posten visas inte eftersom den ligger utanför bokmärket som specificerats av innehållsförteckningen.
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
# Ett TOC-fält kan skapa en post i sin innehållsförteckning för varje SEQ-fält som finns i dokumentet.
# Varje post innehåller stycket som inkluderar SEQ-fältet och sidnumret där fältet visas.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# SEQ-fält visar ett räknare som ökas vid varje SEQ-fält.
# Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
# identifierad av SEQ-fältets egenskap "SequenceIdentifier".
# Använd egenskapen "TableOfFiguresLabel" för att namnge en huvudsekvens för TOC.
# Nu kommer detta TOC endast att skapa poster från SEQ-fält med deras "SequenceIdentifier" inställd på "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Vi kan namnge en annan SEQ-fältsekvens i egenskapen "PrefixedSequenceIdentifier".
# SEQ-fält från denna prefixsekvens kommer inte att skapa TOC-poster.
# Varje TOC-post som skapas från ett huvudsekvens‑SEQ-fält kommer nu också att visa räknaren som
# prefixsekvensen är för närvarande på det primära sekvens‑SEQ‑fältet som skapade posten.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Varje TOC‑post kommer att visa prefixsekvensens räknare omedelbart till vänster
# av sidnumret som huvudsekvensens SEQ‑fält visas på.
# Vi kan ange en anpassad avgränsare som kommer att visas mellan dessa två tal.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Det finns två sätt att använda SEQ‑fält för att fylla i denna TOC.
# 1 -  Infoga ett SEQ‑fält som tillhör TOC:s prefixsekvens:
# Detta fält kommer att öka SEQ‑sekvensräkningen för "PrefixSequence" med 1.
# Eftersom detta fält inte tillhör den identifierade huvudsekvensen
# av TOC:s egenskap "TableOfFiguresLabel", kommer det inte att visas som en post.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 -  Infoga ett SEQ‑fält som tillhör TOC:s huvudsekvens:
# Detta SEQ‑fält kommer att skapa en post i TOC.
# TOC‑posten kommer att innehålla det stycke som SEQ‑fältet finns i samt sidnumret där det visas.
# Denna post kommer också att visa räknaren som prefixsekvensen för närvarande har,
# separerad från sidnumret av värdet i TOC:s egenskap SeqenceSeparator.
# "PrefixSequence"‑räkningen är 1, detta huvudsekvens‑SEQ‑fält är på sida 2,
# och avgränsaren är ">", så posten kommer att visa "1>2".
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Infoga en sida, öka prefixsekvensen med 2, och infoga ett SEQ‑fält för att därefter skapa en TOC‑post.
# Prefixsekvensen är nu 2, och huvudsekvens‑SEQ‑fältet är på sida 3,
# så TOC‑posten kommer att visa "2>3" vid dess sidräkning.
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

