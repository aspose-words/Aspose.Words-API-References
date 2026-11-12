---
title: PageExtractOptions.unlink_pages_number_fields property
linktitle: unlink_pages_number_fields property
articleTitle: unlink_pages_number_fields property
second_title: Aspose.Words for Python
description: "PageExtractOptions.unlink_pages_number_fields property. Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values"
type: docs
weight: 20
url: /ru/python-net/aspose.words/pageextractoptions/unlink_pages_number_fields/
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

* module [aspose.words](../../)
* class [PageExtractOptions](../)

