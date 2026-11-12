---
title: StructuredDocumentTag.is_temporary property
linktitle: is_temporary property
articleTitle: is_temporary property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_temporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /ru/python-net/aspose.words.markup/structureddocumenttag/is_temporary/
---

## StructuredDocumentTag.is_temporary property

Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents
are modified.



```python
@property
def is_temporary(self) -> bool:
    ...

@is_temporary.setter
def is_temporary(self, value: bool):
    ...

```

### Examples

Shows how to make single-use controls.

```python
doc = aw.Document()
# Вставьте структурированный тег документа простого текста,
# который будет выступать в качестве простой текстовой формы, в которую пользователь может вводить текст.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Установите свойство "IsTemporary" в значение "true", чтобы тег структурированного документа исчез и
# встроить его содержимое в документ после того, как пользователь отредактирует его один раз в Microsoft Word.
# Установите свойство "IsTemporary" в значение "false", чтобы позволить пользователю редактировать содержимое
# тега структурированного документа любое количество раз.
tag.is_temporary = is_temporary
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please enter text: ')
builder.insert_node(tag)
# Вставьте ещё один тег структурированного документа в виде флажка и установите его состояние по умолчанию в "checked".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
tag.checked = True
# Установите свойство "IsTemporary" в значение "true", чтобы флажок превратился в символ
# после того, как пользователь щёлкнет по нему в Microsoft Word.
# Установите свойство "IsTemporary" в значение "false", чтобы позволить пользователю щёлкать по флажку любое количество раз.
tag.is_temporary = is_temporary
builder.write('\nPlease click the check box: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.IsTemporary.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

