---
title: OutlineLevel enumeration
linktitle: OutlineLevel enumeration
articleTitle: OutlineLevel enumeration
second_title: Aspose.Words for Python
description: "aspose.words.OutlineLevel enumeration. Specifies the outline level of a paragraph in the document."
type: docs
weight: 890
url: /ru/python-net/aspose.words/outlinelevel/
---

## OutlineLevel enumeration

Specifies the outline level of a paragraph in the document.


### Members

| Name | Description |
| --- | --- |
| LEVEL1 | The paragraph is at the outline level 1 (topmost level). |
| LEVEL2 | The paragraph is at the outline level 2. |
| LEVEL3 | The paragraph is at the outline level 3. |
| LEVEL4 | The paragraph is at the outline level 4. |
| LEVEL5 | The paragraph is at the outline level 5. |
| LEVEL6 | The paragraph is at the outline level 6. |
| LEVEL7 | The paragraph is at the outline level 7. |
| LEVEL8 | The paragraph is at the outline level 8. |
| LEVEL9 | The paragraph is at the outline level 9. |
| BODY_TEXT | The paragraph is at the level of the main text. |

### Examples

Shows how to configure paragraph outline levels to create collapsible text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# У каждого абзаца есть OutlineLevel, который может быть любым числом от 1 до 9 или иметь значение по умолчанию "BodyText".
# Установка свойства в одно из нумерованных значений покажет стрелку слева.
# в начале абзаца.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL1
builder.writeln('Paragraph outline level 1.')
# Уровень 1 — самый верхний уровень. Если ниже абзаца более высокого уровня находится абзац с более низким уровнем,
# сворачивание абзаца более высокого уровня свернёт абзац более низкого уровня.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL2
builder.writeln('Paragraph outline level 2.')
# Два абзаца одного уровня не будут сворачиваться друг с другом,
# и стрелки не сворачивают абзацы, на которые указывают.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL3
builder.writeln('Paragraph outline level 3.')
builder.writeln('Paragraph outline level 3.')
# Значение по умолчанию "BodyText" является самым низким, и любой абзац любого уровня может его свернуть.
builder.paragraph_format.outline_level = aw.OutlineLevel.BODY_TEXT
builder.writeln('Paragraph at main text level.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphOutlineLevel.docx')
```

### See Also

* module [aspose.words](../)

