---
title: Paragraph.break_is_style_separator property
linktitle: break_is_style_separator property
articleTitle: break_is_style_separator property
second_title: Aspose.Words for Python
description: "Paragraph.break_is_style_separator property. True if this paragraph break is a Style Separator"
type: docs
weight: 20
url: /ru/python-net/aspose.words/paragraph/break_is_style_separator/
---

## Paragraph.break_is_style_separator property

True if this paragraph break is a Style Separator. A style separator allows one
paragraph to consist of parts that have different paragraph styles.


```python
@property
def break_is_style_separator(self) -> bool:
    ...

```

### Examples

Shows how to write text to the same line as a TOC heading and have it not show up in the TOC.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_table_of_contents('\\o \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Вставьте абзац со стилем, который TOC распознает как запись.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
# Обе эти строки находятся в одном абзаце и поэтому появятся в одной записи TOC.
builder.write('Heading 1. ')
builder.write('Will appear in the TOC. ')
# Если мы вставим разделитель стиля, мы можем написать больше текста в том же абзаце
# и использовать другой стиль, не отображающийся в оглавлении.
# Если мы применим стиль заголовка после разделителя, мы можем создать несколько записей оглавления из одной строки текста документа.
builder.insert_style_separator()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.QUOTE
builder.write("Won't appear in the TOC. ")
self.assertTrue(doc.first_section.body.first_paragraph.break_is_style_separator)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.BreakIsStyleSeparator.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

