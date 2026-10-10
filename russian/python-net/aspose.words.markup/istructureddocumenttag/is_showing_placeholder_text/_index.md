---
title: IStructuredDocumentTag.is_showing_placeholder_text property
linktitle: is_showing_placeholder_text property
articleTitle: is_showing_placeholder_text property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.is_showing_placeholder_text property. Specifies whether the content of this SDT shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT)."
type: docs
weight: 50
url: /ru/python-net/aspose.words.markup/istructureddocumenttag/is_showing_placeholder_text/
---

## IStructuredDocumentTag.is_showing_placeholder_text property

Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text
(as opposed to regular text contents within the SDT). 


if set to true, this state shall be resumed (showing placeholder text) upon opening this document.




```python
@property
def is_showing_placeholder_text(self) -> bool:
    ...

@is_showing_placeholder_text.setter
def is_showing_placeholder_text(self, value: bool):
    ...

```

### Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```python
doc = aw.Document()
# Вставьте структурированный тег документа простого текста типа "PlainText", который будет функционировать как текстовое поле.
# Содержимое, которое он будет отображать по умолчанию, — подсказка "Click here to enter text.".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Мы можем заставить тег отображать содержимое строительного блока вместо текста по умолчанию.
# Сначала добавьте строительный блок с содержимым в документ глоссария.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'Custom Placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.append_child(aw.Body(glossary_doc))
substitute_block.first_section.body.append_paragraph('Custom placeholder text.')
glossary_doc.append_child(substitute_block)
# Затем используйте свойство "PlaceholderName" структурированного тега документа, чтобы сослаться на этот строительный блок по имени.
tag.placeholder_name = 'Custom Placeholder'
# Если "PlaceholderName" ссылается на существующий блок в глоссарии родительского документа,
# мы сможем проверить строительный блок через свойство "Placeholder".
self.assertEqual(substitute_block, tag.placeholder)
# Установите свойство "IsShowingPlaceholderText" в значение "true", чтобы рассматривать
# текущие содержимое структурированного тега документа как текст-заполнитель.
# Это означает, что щелчок по текстовому полю в Microsoft Word сразу выделит всё содержимое тега.
# Установите свойство "IsShowingPlaceholderText" в значение "false", чтобы получить
# структурированный тег, рассматривающий его содержимое как уже введённый пользователем текст.
# Щелчок по этому тексту в Microsoft Word разместит мигающий курсор в выбранном месте.
tag.is_showing_placeholder_text = is_showing_placeholder_text
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlaceholderBuildingBlock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

