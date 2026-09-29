---
title: PageExtractOptions.update_page_starting_number property
linktitle: update_page_starting_number property
articleTitle: update_page_starting_number property
second_title: Aspose.Words for Python
description: "PageExtractOptions.update_page_starting_number property. Specifies whether the start page number in the resulting document shall be updated"
type: docs
weight: 30
url: /sv/python-net/aspose.words/pageextractoptions/update_page_starting_number/
---

## PageExtractOptions.update_page_starting_number property

Specifies whether the start page number in the resulting document shall be updated.
Default value is ``True``.



```python
@property
def update_page_starting_number(self) -> bool:
    ...

@update_page_starting_number.setter
def update_page_starting_number(self, value: bool):
    ...

```

### Examples

Show how to reset the initial page numbering and save the NUMPAGE field.

```python
doc = aw.Document(file_name=MY_DIR + 'Page fields.docx')
# Standardbeteende:
# Den extraherade sidnumreringen är densamma som i originaldokumentet, som om vi hade valt "Print 2 pages" i MS Word.
# Startsidnumret kommer att sättas till 2 och fältet som indikerar antalet sidor kommer att tas bort
# och ersättas med ett konstant värde lika med antalet sidor.
extracted_doc1 = doc.extract_pages(index=1, count=1)
extracted_doc1.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Default.docx')
# Ändrat beteende:
# Den extraherade sidnumreringen återställs och en ny börjar,
# som om vi hade kopierat innehållet på den andra sidan och klistrat in det i ett nytt dokument.
# Startsidnumret kommer att sättas till 1 och fältet som indikerar antalet sidor kommer att lämnas oförändrat
# och kommer att visa det aktuella antalet sidor.
extract_options = aw.PageExtractOptions()
extract_options.update_page_starting_number = False
extract_options.unlink_pages_number_fields = False
extracted_doc2 = doc.extract_pages(index=1, count=1, options=extract_options)
extracted_doc2.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Options.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageExtractOptions](../)

