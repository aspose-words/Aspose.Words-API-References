---
title: FieldToc.use_paragraph_outline_level property
linktitle: use_paragraph_outline_level property
articleTitle: use_paragraph_outline_level property
second_title: Aspose.Words for Python
description: "FieldToc.use_paragraph_outline_level property. Gets or sets whether to use the applied paragraph outline level."
type: docs
weight: 170
url: /sv/python-net/aspose.words.fields/fieldtoc/use_paragraph_outline_level/
---

## FieldToc.use_paragraph_outline_level property

Gets or sets whether to use the applied paragraph outline level.


```python
@property
def use_paragraph_outline_level(self) -> bool:
    ...

@use_paragraph_outline_level.setter
def use_paragraph_outline_level(self, value: bool):
    ...

```

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

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

