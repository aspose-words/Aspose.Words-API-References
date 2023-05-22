---
title: ImportFormatOptions.keep_source_numbering property
linktitle: keep_source_numbering property
articleTitle: keep_source_numbering property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.keep_source_numbering property. Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents"
type: docs
weight: 60
url: /python-net/aspose.words/importformatoptions/keep_source_numbering/
---

## ImportFormatOptions.keep_source_numbering property

Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and
destination documents.
The default value is ``False``.



### Examples

Shows how to import a document with numbered lists.

```python
src_doc = aw.Document(MY_DIR + "List source.docx")
dst_doc = aw.Document(MY_DIR + "List destination.docx")

self.assertEqual(4, dst_doc.lists.count)

options = aw.ImportFormatOptions()

# If there is a clash of list styles, apply the list format of the source document.
# Set the "keep_source_numbering" property to "False" to not import any list numbers into the destination document.
# Set the "keep_source_numbering" property to "True" import all clashing
# list style numbering with the same appearance that it had in the source document.
options.keep_source_numbering = is_keep_source_numbering

dst_doc.append_document(src_doc, aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, options)
dst_doc.update_list_labels()

if is_keep_source_numbering:
    self.assertEqual(5, dst_doc.lists.count)
else:
    self.assertEqual(4, dst_doc.lists.count)
```

Shows how resolve a clash when importing documents that have lists with the same list definition identifier.

```python
src_doc = aw.Document(MY_DIR + "List with the same definition identifier - source.docx")
dst_doc = aw.Document(MY_DIR + "List with the same definition identifier - destination.docx")

# Set the "keep_source_numbering" property to "True" to apply a different list definition ID
# to identical styles as Aspose.Words imports them into destination documents.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = True

dst_doc.append_document(src_doc, aw.ImportFormatMode.USE_DESTINATION_STYLES, import_format_options)
dst_doc.update_list_labels()
```

Shows how to resolve list numbering clashes in source and destination documents.

```python
# Open a document with a custom list numbering scheme, and then clone it.
# Since both have the same numbering format, the formats will clash if we import one document into the other.
src_doc = aw.Document(MY_DIR + "Custom list numbering.docx")
dst_doc = src_doc.clone()

# When we import the document's clone into the original and then append it,
# then the two lists with the same list format will join.
# If we set the "keep_source_numbering" flag to "False", then the list from the document clone
# that we append to the original will carry on the numbering of the list we append it to.
# This will effectively merge the two lists into one.
# If we set the "keep_source_numbering" flag to "True", then the document clone
# list will preserve its original numbering, making the two lists appear as separate lists.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = keep_source_numbering

importer = aw.NodeImporter(src_doc, dst_doc, aw.ImportFormatMode.KEEP_DIFFERENT_STYLES, import_format_options)
for paragraph in src_doc.first_section.body.paragraphs:
    paragraph = paragraph.as_paragraph()
    imported_node = importer.import_node(paragraph, True)
    dst_doc.first_section.body.append_child(imported_node)

dst_doc.update_list_labels()

if keep_source_numbering:
    self.assertEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dst_doc.first_section.body.to_string(aw.SaveFormat.TEXT).strip())
else:
    self.assertEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dst_doc.first_section.body.to_string(aw.SaveFormat.TEXT).strip())
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

