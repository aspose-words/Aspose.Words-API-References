---
title: FieldSection class
linktitle: FieldSection class
articleTitle: FieldSection class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSection class. Implements the SECTION field"
type: docs
weight: 900
url: /fr/python-net/aspose.words.fields/fieldsection/
---

## FieldSection class

Implements the SECTION field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Retrieves the number of the current section.


**Inheritance:** [FieldSection](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSection()](./__init__/#default) | The default constructor. |

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

Shows how to use SECTION and SECTIONPAGES fields to number pages by sections.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.RIGHT
# Un champ SECTION affiche le numéro de la section dans laquelle il se trouve.
builder.write('Section ')
field_section = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SECTION, update_field=True).as_field_section()
self.assertEqual(' SECTION ', field_section.get_field_code())
# Un champ PAGE affiche le numéro de la page dans laquelle il se trouve.
builder.write('\nPage ')
field_page = builder.insert_field(field_type=aw.fields.FieldType.FIELD_PAGE, update_field=True).as_field_page()
self.assertEqual(' PAGE ', field_page.get_field_code())
# Un champ SECTIONPAGES affiche le nombre de pages que couvre la section dans laquelle il se trouve.
builder.write(' of ')
field_section_pages = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SECTION_PAGES, update_field=True).as_field_section_pages()
self.assertEqual(' SECTIONPAGES ', field_section_pages.get_field_code())
# Sortir de l'en-tête pour revenir au document principal et insérer deux pages.
# Toutes ces pages seront dans la première section. Nos champs, qui apparaissent une fois dans chaque en-tête,
# numérotent les pages actuelles/totales de cette section.
builder.move_to_document_end()
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Nous pouvons insérer une nouvelle section avec le constructeur de document comme ceci.
# Cela affectera les valeurs affichées dans les champs SECTION et SECTIONPAGES dans tous les en-têtes à venir.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
# Le champ PAGE continuera de compter les pages dans l'ensemble du document.
# Nous pouvons réinitialiser manuellement son compteur à chaque section pour suivre les pages section par section.
builder.current_section.page_setup.restart_page_numbering = True
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SECTION.SECTIONPAGES.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

