---
title: StructuredDocumentTag.tag property
linktitle: tag property
articleTitle: tag property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.tag property. Specifies a tag associated with the current SDT node"
type: docs
weight: 280
url: /ru/python-net/aspose.words.markup/structureddocumenttag/tag/
---

## StructuredDocumentTag.tag property

Specifies a tag associated with the current SDT node.
Can not be ``None``.



```python
@property
def tag(self) -> str:
    ...

@tag.setter
def tag(self, value: str):
    ...

```

### Remarks

A tag is an arbitrary string which applications can associate with SDT
in order to identify it without providing a visible friendly name.


### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```python
doc = aw.Document()
# Создайте структурированный тег документа, который будет содержать простой текст.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Установите заголовок и цвет рамки, которая появляется при наведении мыши на структурированный тег документа в Microsoft Word.
tag.title = 'My plain text'
tag.color = aspose.pydrawing.Color.magenta
# Установите тег для этого структурированного тега документа, который доступен
# в виде XML‑элемента с именем "tag", со строкой ниже в его атрибуте "@val".
tag.tag = 'MyPlainTextSDT'
# У каждого структурированного тега документа есть случайный уникальный идентификатор.
self.assertTrue(tag.id > 0)
# Установите шрифт для текста внутри структурированного тега документа.
tag.contents_font.name = 'Arial'
# Установите шрифт для текста в конце структурированного тега документа.
# Любой текст, который мы вводим в теле документа после выхода из тега с помощью клавиш‑стрелок, будет использовать этот шрифт.
tag.end_character_font.name = 'Arial Black'
# По умолчанию это false, и нажатие Enter внутри структурированного тега документа ничего не делает.
# Когда установлено в true, наш структурированный тег документа может содержать несколько строк.
# Установите свойство "Multiline" в "false", чтобы разрешить содержимое
# этого структурированного тега документа занимать одну строку.
# Установите свойство "Multiline" в "true", чтобы тег мог содержать несколько строк контента.
tag.multiline = True
# Установите свойство "Appearance" в "SdtAppearance.Tags", чтобы отображать теги вокруг содержимого.
# По умолчанию структурированный тег документа отображается как BoundingBox.
tag.appearance = aw.markup.SdtAppearance.TAGS
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
# Вставьте клон нашего структурированного тега документа в новый абзац.
tag_clone = tag.clone(True).as_structured_document_tag()
builder.insert_paragraph()
builder.insert_node(tag_clone)
# Используйте метод "RemoveSelfOnly", чтобы удалить структурированный тег документа, оставив его содержимое в документе.
tag_clone.remove_self_only()
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlainText.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

