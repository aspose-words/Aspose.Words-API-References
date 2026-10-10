---
title: PageExtractOptions class
linktitle: PageExtractOptions class
articleTitle: PageExtractOptions class
second_title: Aspose.Words for Python
description: "aspose.words.PageExtractOptions class. Allows to specify options for document page extracting."
type: docs
weight: 920
url: /it/python-net/aspose.words/pageextractoptions/
---

## PageExtractOptions class

Allows to specify options for document page extracting.


### Constructors
| Name | Description |
| --- | --- |
| [PageExtractOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [unlink_pages_number_fields](./unlink_pages_number_fields/) | Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values. Default value is ``True``. |
| [update_page_starting_number](./update_page_starting_number/) | Specifies whether the start page number in the resulting document shall be updated. Default value is ``True``. |

### Examples

Show how to reset the initial page numbering and save the NUMPAGE field.

```python
doc = aw.Document(file_name=MY_DIR + 'Page fields.docx')
# Comportamento predefinito:
# La numerazione delle pagine estratta è la stessa del documento originale, come se avessimo selezionato "Print 2 pages" in MS Word.
# La pagina iniziale sarà impostata a 2 e il campo che indica il numero di pagine sarà rimosso
# e sostituito con un valore costante pari al numero di pagine.
extracted_doc1 = doc.extract_pages(index=1, count=1)
extracted_doc1.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Default.docx')
# Comportamento modificato:
# La numerazione delle pagine estratta viene reimpostata e ne inizia una nuova,
# come se avessimo copiato il contenuto della seconda pagina e incollato in un nuovo documento.
# La pagina iniziale sarà impostata a 1 e il campo che indica il numero di pagine rimarrà invariato
# e mostrerà il numero corrente di pagine.
extract_options = aw.PageExtractOptions()
extract_options.update_page_starting_number = False
extract_options.unlink_pages_number_fields = False
extracted_doc2 = doc.extract_pages(index=1, count=1, options=extract_options)
extracted_doc2.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Options.docx')
```

### See Also

* module [aspose.words](../)

