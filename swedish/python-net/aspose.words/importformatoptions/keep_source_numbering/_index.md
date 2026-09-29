---
title: ImportFormatOptions.keep_source_numbering property
linktitle: keep_source_numbering property
articleTitle: keep_source_numbering property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.keep_source_numbering property. Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents"
type: docs
weight: 70
url: /sv/python-net/aspose.words/importformatoptions/keep_source_numbering/
---

## ImportFormatOptions.keep_source_numbering property

Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and
destination documents.
The default value is ``False``.



```python
@property
def keep_source_numbering(self) -> bool:
    ...

@keep_source_numbering.setter
def keep_source_numbering(self, value: bool):
    ...

```

### Examples

Shows how to import a document with numbered lists.

```python
src_doc = aw.Document(file_name=MY_DIR + 'List source.docx')
dst_doc = aw.Document(file_name=MY_DIR + 'List destination.docx')
self.assertEqual(4, dst_doc.lists.count)
options = aw.ImportFormatOptions()
# Om det finns en krock mellan liststilar, tillämpa listformatet från källdokumentet.
# Ställ in egenskapen "KeepSourceNumbering" till "false" för att inte importera några listnummer till måldokumentet.
# Ställ in egenskapen "KeepSourceNumbering" till "true" importera alla konflikter
# liststilnumrering med samma utseende som den hade i källdokumentet.
options.keep_source_numbering = is_keep_source_numbering
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=options)
dst_doc.update_list_labels()
self.assertEqual(5 if is_keep_source_numbering else 4, dst_doc.lists.count)
```

Shows how resolve a clash when importing documents that have lists with the same list definition identifier.

```python
src_doc = aw.Document(file_name=MY_DIR + 'List with the same definition identifier - source.docx')
dst_doc = aw.Document(file_name=MY_DIR + 'List with the same definition identifier - destination.docx')
# Ställ in egenskapen "KeepSourceNumbering" till "true" för att tillämpa ett annat listdefinition‑ID
# till identiska stilar som Aspose.Words importerar dem till destinationsdokument.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = True
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES, import_format_options=import_format_options)
dst_doc.update_list_labels()
```

Shows how to resolve list numbering clashes in source and destination documents.

```python
# Öppna ett dokument med ett anpassat listnumreringsschema och klona det sedan.
# Eftersom båda har samma numreringsformat kommer formaten att kollidera om vi importerar ett dokument till det andra.
src_doc = aw.Document(file_name=MY_DIR + 'Custom list numbering.docx')
dst_doc = src_doc.clone()
# När vi importerar dokumentklonen till originalet och sedan lägger till den,
# kommer de två listorna med samma listformat att slås samman.
# Om vi ställer in flaggan "KeepSourceNumbering" till "false", så kommer listan från dokumentklonen
# som vi lägger till originalet att fortsätta numreringen av den lista vi lägger till den i.
# Detta kommer effektivt att slå samman de två listorna till en.
# Om vi ställer in flaggan "KeepSourceNumbering" till "true", så kommer dokumentklonen
# listan bevarar sin ursprungliga numrering, vilket gör att de två listorna visas som separata listor.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = keep_source_numbering
importer = aw.NodeImporter(src_doc=src_doc, dst_doc=dst_doc, import_format_mode=aw.ImportFormatMode.KEEP_DIFFERENT_STYLES, import_format_options=import_format_options)
for paragraph in src_doc.first_section.body.paragraphs:
    paragraph = paragraph.as_paragraph()
    imported_node = importer.import_node(paragraph, True)
    dst_doc.first_section.body.append_child(imported_node)
dst_doc.update_list_labels()
if keep_source_numbering:
    self.assertEqual('6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4\r\n' + '6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4', dst_doc.first_section.body.to_string(save_format=aw.SaveFormat.TEXT).strip())
else:
    self.assertEqual('6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4\r\n' + '10. Item 1\r\n' + '11. Item 2 \r\n' + '12. Item 3\r\n' + '13. Item 4', dst_doc.first_section.body.to_string(save_format=aw.SaveFormat.TEXT).strip())
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

