---
title: DocumentDirection enumeration
linktitle: DocumentDirection enumeration
articleTitle: DocumentDirection enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.DocumentDirection enumeration. Allows to specify the direction to flow the text in a document."
type: docs
weight: 30
url: /ru/python-net/aspose.words.loading/documentdirection/
---

## DocumentDirection enumeration

Allows to specify the direction to flow the text in a document.


### Members

| Name | Description |
| --- | --- |
| LEFT_TO_RIGHT | Left to right direction. |
| RIGHT_TO_LEFT | Right to left direction. |
| AUTO | Auto-detect direction. |

### Examples

Shows how to detect plaintext document text direction.

```python
# Создайте объект "TxtLoadOptions", который мы можем передать конструктору документа
# чтобы изменить способ загрузки обычного текстового документа.
load_options = aw.loading.TxtLoadOptions()
# Установите свойство "DocumentDirection" в значение "DocumentDirection.Auto", которое автоматически определяет
# направление каждого абзаца текста, который Aspose.Words загружает из обычного текста.
# Свойство "Bidi" каждого абзаца будет хранить его направление.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Обнаруживать иврит как текст справа налево.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Обнаруживать английский текст как справа налево.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words.loading](../)

