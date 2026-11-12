---
title: ParagraphFormat.line_spacing_rule property
linktitle: line_spacing_rule property
articleTitle: line_spacing_rule property
second_title: Aspose.Words for Python
description: "ParagraphFormat.line_spacing_rule property. Gets or sets the line spacing for the paragraph."
type: docs
weight: 200
url: /ru/python-net/aspose.words/paragraphformat/line_spacing_rule/
---

## ParagraphFormat.line_spacing_rule property

Gets or sets the line spacing for the paragraph.


```python
@property
def line_spacing_rule(self) -> aspose.words.LineSpacingRule:
    ...

@line_spacing_rule.setter
def line_spacing_rule(self, value: aspose.words.LineSpacingRule):
    ...

```

### Examples

Shows how to work with line spacing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ниже представлены три правила межстрочного интервала, которые мы можем задать с помощью
# свойства "LineSpacingRule" абзаца для настройки интервала между абзацами.
# 1 -  Установите минимальное количество отступов.
# Это добавит вертикальный отступ к строкам текста любого размера
# которые слишком малы, чтобы поддерживать минимальную высоту строки.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.AT_LEAST
builder.paragraph_format.line_spacing = 20
builder.writeln('Minimum line spacing of 20.')
builder.writeln('Minimum line spacing of 20.')
# 2 -  Установите точный отступ.
# Использование размеров шрифта, слишком больших для отступа, приведёт к усечению текста.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.EXACTLY
builder.paragraph_format.line_spacing = 5
builder.writeln('Line spacing of exactly 5.')
builder.writeln('Line spacing of exactly 5.')
# 3 -  Установите отступ как кратный значению стандартного межстрочного интервала, которое по умолчанию равно 12 пунктов.
# Такой тип отступа будет масштабироваться под разные размеры шрифта.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.MULTIPLE
builder.paragraph_format.line_spacing = 18
builder.writeln('Line spacing of 1.5 default lines.')
builder.writeln('Line spacing of 1.5 default lines.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LineSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

