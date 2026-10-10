---
title: ParagraphFormat.widow_control property
linktitle: widow_control property
articleTitle: widow_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.widow_control property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /ru/python-net/aspose.words/paragraphformat/widow_control/
---

## ParagraphFormat.widow_control property

True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.


```python
@property
def widow_control(self) -> bool:
    ...

@widow_control.setter
def widow_control(self, value: bool):
    ...

```

### Examples

Shows how to enable widow/orphan control for a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Когда мы пишем текст, который не помещается на одну страницу, одна строка может перейти на следующую страницу.
# Одинокая строка, оказавшаяся на следующей странице, называется \"Orphan\" (сиротой),
# а предыдущая строка, от которой «сирота» оторвалась, называется \"Widow\" (вдовой).
# Мы можем исправить «сирот» и «вдовы», переставив текст с помощью размера шрифта, интервалов или полей страницы.
# Если мы хотим сохранить размеры документа, мы можем установить этот флаг в \"true\"
# чтобы переместить «вдовы» на ту же страницу, что и их соответствующие «сироты».
# Оставив этот флаг в значении \"false\", пары «вдова/сирота» останутся в тексте.
# Каждый абзац имеет эту настройку, доступную в Microsoft Word через Главная -> Абзац -> Параметры абзаца
# (кнопка в правом нижнем углу вкладки \"Paragraph\") -> \"Widow/Orphan control\".
builder.paragraph_format.widow_control = widow_control
# Вставьте текст, который создаёт «сироту» и «вдову».
builder.font.size = 68
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.WidowControl.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

