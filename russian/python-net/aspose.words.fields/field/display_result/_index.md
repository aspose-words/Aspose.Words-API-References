---
title: Field.display_result property
linktitle: display_result property
articleTitle: display_result property
second_title: Aspose.Words for Python
description: "Field.display_result property. Gets the text that represents the displayed field result."
type: docs
weight: 10
url: /ru/python-net/aspose.words.fields/field/display_result/
---

## Field.display_result property

Gets the text that represents the displayed field result.


```python
@property
def display_result(self) -> str:
    ...

```

### Remarks

The [Document.update_list_labels()](../../../aspose.words/document/update_list_labels/#default) method must be called to obtain correct value for the
[FieldListNum](../../fieldlistnum/), [FieldAutoNum](../../fieldautonum/), [FieldAutoNumOut](../../fieldautonumout/) and [FieldAutoNumLgl](../../fieldautonumlgl/) fields.



### Examples

Shows how to get the real text that a field displays in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('This document was written by ')
field_author = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field_author.author_name = 'John Doe'
# Мы можем использовать свойство DisplayResult, чтобы проверить, какой точный текст
# поле отобразит вместо себя в документе.
self.assertEqual('', field_author.display_result)
# Поля не поддерживают точные значения результатов в реальном времени.
# Чтобы убедиться, что наши поля отображают точные результаты в любой момент,
# например, непосредственно перед сохранением, нам необходимо обновлять их вручную.
field_author.update()
self.assertEqual('John Doe', field_author.display_result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.DisplayResult.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

