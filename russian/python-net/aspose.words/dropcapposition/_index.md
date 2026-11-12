---
title: DropCapPosition enumeration
linktitle: DropCapPosition enumeration
articleTitle: DropCapPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.DropCapPosition enumeration. Specifies the position for a drop cap text."
type: docs
weight: 350
url: /ru/python-net/aspose.words/dropcapposition/
---

## DropCapPosition enumeration

Specifies the position for a drop cap text.


### Members

| Name | Description |
| --- | --- |
| NONE | The paragraph does not have a drop cap. |
| NORMAL | The drop cap is positioned inside the text margin on the anchor paragraph. |
| MARGIN | The drop cap is positioned outside the text margin on the anchor paragraph. |

### Examples

Shows how to create a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте один абзац с большой буквой, с которой начинается текст во втором и третьем абзацах.
builder.font.size = 54
builder.writeln('L')
builder.font.size = 18
builder.writeln('orem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ')
builder.writeln('Ut enim ad minim veniam, quis nostrud exercitation ' + 'ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# В настоящее время второй и третий абзацы будут отображаться под первым.
# Мы можем преобразовать первый абзац в букву‑капитель для остальных абзацев через его объект "ParagraphFormat".
# Установите свойство "DropCapPosition" в значение "DropCapPosition.Margin", чтобы разместить букву‑капитель
# вне левого поля страницы, если наш текст читается слева направо.
# Установите свойство "DropCapPosition" в значение "DropCapPosition.Normal", чтобы разместить букву‑капитель внутри полей страницы
# и обтекать остальной текст вокруг неё.
# "DropCapPosition.None" является состоянием по умолчанию для всех абзацев.
format = doc.first_section.body.first_paragraph.paragraph_format
format.drop_cap_position = drop_cap_position
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.DropCap.docx')
```

### See Also

* module [aspose.words](../)

