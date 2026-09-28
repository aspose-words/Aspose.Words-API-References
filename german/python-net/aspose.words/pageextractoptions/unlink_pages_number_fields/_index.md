---
title: PageExtractOptions.unlink_pages_number_fields property
linktitle: unlink_pages_number_fields property
articleTitle: unlink_pages_number_fields property
second_title: Aspose.Words for Python
description: "PageExtractOptions.unlink_pages_number_fields property. Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values"
type: docs
weight: 20
url: /de/python-net/aspose.words/pageextractoptions/unlink_pages_number_fields/
---

## PageExtractOptions.unlink_pages_number_fields property

Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values.
Default value is ``True``.



```python
@property
def unlink_pages_number_fields(self) -> bool:
    ...

@unlink_pages_number_fields.setter
def unlink_pages_number_fields(self, value: bool):
    ...

```

### Examples

Show how to reset the initial page numbering and save the NUMPAGE field.

```python
doc = aw.Document(file_name=MY_DIR + 'Page fields.docx')
# Standardverhalten:
# Die extrahierte Seitennummerierung ist dieselbe wie im Originaldokument, als hätten wir in MS Word \"Print 2 pages\" ausgewählt.
# Die Startseite wird auf 2 gesetzt und das Feld, das die Anzahl der Seiten angibt, wird entfernt
# und durch einen konstanten Wert ersetzt, der der Seitenzahl entspricht.
extracted_doc1 = doc.extract_pages(index=1, count=1)
extracted_doc1.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Default.docx')
# Geändertes Verhalten:
# Die extrahierte Seitennummerierung wird zurückgesetzt und eine neue beginnt,
# als hätten wir den Inhalt der zweiten Seite kopiert und in ein neues Dokument eingefügt.
# Die Startseite wird auf 1 gesetzt und das Feld, das die Anzahl der Seiten angibt, bleibt unverändert
# und zeigt die aktuelle Seitenzahl an.
extract_options = aw.PageExtractOptions()
extract_options.update_page_starting_number = False
extract_options.unlink_pages_number_fields = False
extracted_doc2 = doc.extract_pages(index=1, count=1, options=extract_options)
extracted_doc2.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Options.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageExtractOptions](../)

