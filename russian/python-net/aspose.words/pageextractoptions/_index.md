---
title: PageExtractOptions class
linktitle: PageExtractOptions class
articleTitle: PageExtractOptions class
second_title: Aspose.Words for Python
description: "aspose.words.PageExtractOptions class. Allows to specify options for document page extracting."
type: docs
weight: 920
url: /ru/python-net/aspose.words/pageextractoptions/
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
# Поведение по умолчанию:
# Извлечённая нумерация страниц совпадает с оригинальным документом, как будто мы выбрали "Print 2 pages" в MS Word.
# Номер начальной страницы будет установлен в 2, а поле, указывающее количество страниц, будет удалено
# и заменено постоянным значением, равным количеству страниц.
extracted_doc1 = doc.extract_pages(index=1, count=1)
extracted_doc1.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Default.docx')
# Изменённое поведение:
# Извлечённая нумерация страниц сбрасывается, и начинается новая,
# как будто мы скопировали содержимое второй страницы и вставили его в новый документ.
# Номер начальной страницы будет установлен в 1, а поле, указывающее количество страниц, останется без изменений
# и будет показывать текущее количество страниц.
extract_options = aw.PageExtractOptions()
extract_options.update_page_starting_number = False
extract_options.unlink_pages_number_fields = False
extracted_doc2 = doc.extract_pages(index=1, count=1, options=extract_options)
extracted_doc2.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Options.docx')
```

### See Also

* module [aspose.words](../)

