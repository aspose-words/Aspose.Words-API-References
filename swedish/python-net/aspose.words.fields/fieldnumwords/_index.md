---
title: FieldNumWords class
linktitle: FieldNumWords class
articleTitle: FieldNumWords class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldNumWords class. Implements the NUMWORDS field"
type: docs
weight: 770
url: /sv/python-net/aspose.words.fields/fieldnumwords/
---

## FieldNumWords class

Implements the NUMWORDS field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Retrieves the number of words in the current document, as recorded in the **Words** property of the
built-in document properties.



**Inheritance:** [FieldNumWords](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldNumWords()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to use NUMCHARS, NUMWORDS, NUMPAGES and PAGE fields to track the size of our documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
# Nedan följer tre typer av fält som vi kan använda för att spåra storleken på våra dokument.
# 1 -  Spåra teckenantalet med ett NUMCHARS-fält:
field_num_chars = builder.insert_field(field_type=aw.fields.FieldType.FIELD_NUM_CHARS, update_field=True).as_field_num_chars()
builder.writeln(' characters')
# 2 -  Spåra ordantalet med ett NUMWORDS-fält:
field_num_words = builder.insert_field(field_type=aw.fields.FieldType.FIELD_NUM_WORDS, update_field=True).as_field_num_words()
builder.writeln(' words')
# 3 -  Använd både PAGE- och NUMPAGES-fält för att visa på vilken sida fältet är,
# och det totala antalet sidor i dokumentet:
builder.paragraph_format.alignment = aw.ParagraphAlignment.RIGHT
builder.write('Page ')
field_page = builder.insert_field(field_type=aw.fields.FieldType.FIELD_PAGE, update_field=True).as_field_page()
builder.write(' of ')
field_num_pages = builder.insert_field(field_type=aw.fields.FieldType.FIELD_NUM_PAGES, update_field=True).as_field_num_pages()
self.assertEqual(' NUMCHARS ', field_num_chars.get_field_code())
self.assertEqual(' NUMWORDS ', field_num_words.get_field_code())
self.assertEqual(' NUMPAGES ', field_num_pages.get_field_code())
self.assertEqual(' PAGE ', field_page.get_field_code())
# Dessa fält kommer inte att behålla korrekta värden i realtid
# medan vi redigerar dokumentet programmässigt med Aspose.Words, eller i Microsoft Word.
# Vi måste uppdatera dem varje gång vi behöver se ett aktuellt värde.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.NUMCHARS.NUMWORDS.NUMPAGES.PAGE.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

