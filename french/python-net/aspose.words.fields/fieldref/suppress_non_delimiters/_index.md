---
title: FieldRef.suppress_non_delimiters property
linktitle: suppress_non_delimiters property
articleTitle: suppress_non_delimiters property
second_title: Aspose.Words for Python
description: "FieldRef.suppress_non_delimiters property. Gets or sets whether to suppress non-delimiter characters."
type: docs
weight: 100
url: /fr/python-net/aspose.words.fields/fieldref/suppress_non_delimiters/
---

## FieldRef.suppress_non_delimiters property

Gets or sets whether to suppress non-delimiter characters.


```python
@property
def suppress_non_delimiters(self) -> bool:
    ...

@suppress_non_delimiters.setter
def suppress_non_delimiters(self, value: bool):
    ...

```

### Examples

Shows how to insert REF fields to reference bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='MyBookmark footnote #1')
builder.write('Text that will appear in REF field')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='MyBookmark footnote #2')
builder.end_bookmark('MyBookmark')
builder.move_to_document_start()
# Nous appliquerons un format de liste personnalisé, où le nombre de chevrons indique le niveau de liste dans lequel nous nous trouvons actuellement.
builder.list_format.apply_number_default()
builder.list_format.list_level.number_format = '> \x00'
# Insérez un champ REF qui contiendra le texte de notre signet, agira comme un hyperlien et dupliquera les notes de bas de page du signet.
field = ExField._insert_field_ref(builder, 'MyBookmark', '', '\n')
field.include_note_or_comment = True
field.insert_hyperlink = True
self.assertEqual(' REF  MyBookmark \\f \\h', field.get_field_code())
# Insérez un champ REF et affichez si le signet référencé se trouve au-dessus ou en dessous.
field = ExField._insert_field_ref(builder, 'MyBookmark', 'The referenced paragraph is ', ' this field.\n')
field.insert_relative_position = True
self.assertEqual(' REF  MyBookmark \\p', field.get_field_code())
# Affichez le numéro de liste du signet tel qu'il apparaît dans le document.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number is ", '\n')
field.insert_paragraph_number = True
self.assertEqual(' REF  MyBookmark \\n', field.get_field_code())
# Affichez le numéro de liste du signet, mais en omettant les caractères non délimiteurs, tels que les chevrons.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number, non-delimiters suppressed, is ", '\n')
field.insert_paragraph_number = True
field.suppress_non_delimiters = True
self.assertEqual(' REF  MyBookmark \\n \\t', field.get_field_code())
# Descendez d'un niveau de liste.
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>> \x01'
# Affichez le numéro de liste du signet ainsi que les numéros de tous les niveaux de liste supérieurs.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's full context paragraph number is ", '\n')
field.insert_paragraph_number_in_full_context = True
self.assertEqual(' REF  MyBookmark \\w', field.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Affichez les numéros de niveau de liste entre ce champ REF et le signet qu'il référence.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's relative paragraph number is ", '\n')
field.insert_paragraph_number_in_relative_context = True
self.assertEqual(' REF  MyBookmark \\r', field.get_field_code())
# À la fin du document, le signet apparaîtra ici comme un élément de liste.
builder.writeln('List level above bookmark')
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>>> \x02'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.REF.docx')
```

Shows how to insert REF fields to reference bookmarks (InsertFieldRef).

```python
@staticmethod
def _insert_field_ref(builder, bookmark_name, text_before, text_after):
    builder.write(text_before)
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF, update_field=True).as_field_ref()
    field.bookmark_name = bookmark_name
    builder.write(text_after)
    return field
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldRef](../)

