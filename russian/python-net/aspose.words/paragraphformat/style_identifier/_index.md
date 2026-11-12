---
title: ParagraphFormat.style_identifier property
linktitle: style_identifier property
articleTitle: style_identifier property
second_title: Aspose.Words for Python
description: "ParagraphFormat.style_identifier property. Gets or sets the locale independent style identifier of the paragraph style applied to this formatting."
type: docs
weight: 360
url: /ru/python-net/aspose.words/paragraphformat/style_identifier/
---

## ParagraphFormat.style_identifier property

Gets or sets the locale independent style identifier of the paragraph style applied to this formatting.


```python
@property
def style_identifier(self) -> aspose.words.StyleIdentifier:
    ...

@style_identifier.setter
def style_identifier(self, value: aspose.words.StyleIdentifier):
    ...

```

### Examples

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте оглавление на первую страницу документа.
# Настройте таблицу так, чтобы она захватывала абзацы с заголовками уровней от 1 до 3.
# Также установите, чтобы её элементы были гиперссылками, которые перенаправят нас
# к месту заголовка при щелчке левой кнопкой мыши в Microsoft Word.
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Заполните оглавление, добавив абзацы со стилями заголовков.
# Каждый такой заголовок уровня от 1 до 3 создаст запись в таблице.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 2')
builder.writeln('Heading 3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 3.1.1')
builder.writeln('Heading 3.1.2')
builder.writeln('Heading 3.1.3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 3.1.3.1')
builder.writeln('Heading 3.1.3.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.2')
builder.writeln('Heading 3.3')
# Оглавление — это поле определённого типа, которое необходимо обновить, чтобы отобразить актуальный результат.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

