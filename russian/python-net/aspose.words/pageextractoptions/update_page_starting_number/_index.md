---
title: PageExtractOptions.update_page_starting_number property
linktitle: update_page_starting_number property
articleTitle: update_page_starting_number property
second_title: Aspose.Words for Python
description: "PageExtractOptions.update_page_starting_number property. Specifies whether the start page number in the resulting document shall be updated"
type: docs
weight: 30
url: /ru/python-net/aspose.words/pageextractoptions/update_page_starting_number/
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

