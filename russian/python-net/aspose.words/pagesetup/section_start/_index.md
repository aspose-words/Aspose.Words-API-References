---
title: PageSetup.section_start property
linktitle: section_start property
articleTitle: section_start property
second_title: Aspose.Words for Python
description: "PageSetup.section_start property. Returns or sets the type of section break for the specified object."
type: docs
weight: 390
url: /ru/python-net/aspose.words/pagesetup/section_start/
---

## PageSetup.section_start property

Returns or sets the type of section break for the specified object.


```python
@property
def section_start(self) -> aspose.words.SectionStart:
    ...

@section_start.setter
def section_start(self, value: aspose.words.SectionStart):
    ...

```

### Examples

Shows how to specify how a new section separates itself from the previous.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('This text is in section 1.')
# Типы разрывов разделов определяют, как новый раздел отделяется от предыдущего.
# Ниже представлены пять типов разрывов разделов.
# 1 -  Начинает следующий раздел на новой странице:
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('This text is in section 2.')
self.assertEqual(aw.SectionStart.NEW_PAGE, doc.sections[1].page_setup.section_start)
# 2 -  Начинает следующий раздел на текущей странице:
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln('This text is in section 3.')
self.assertEqual(aw.SectionStart.CONTINUOUS, doc.sections[2].page_setup.section_start)
# 3 -  Начинает следующий раздел на новой чётной странице:
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.writeln('This text is in section 4.')
self.assertEqual(aw.SectionStart.EVEN_PAGE, doc.sections[3].page_setup.section_start)
# 4 -  Начинает следующий раздел на новой нечётной странице:
builder.insert_break(aw.BreakType.SECTION_BREAK_ODD_PAGE)
builder.writeln('This text is in section 5.')
self.assertEqual(aw.SectionStart.ODD_PAGE, doc.sections[4].page_setup.section_start)
# 5 -  Начинает следующий раздел в новой колонке:
columns = builder.page_setup.text_columns
columns.set_count(2)
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_COLUMN)
builder.writeln('This text is in section 6.')
self.assertEqual(aw.SectionStart.NEW_COLUMN, doc.sections[5].page_setup.section_start)
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.SetSectionStart.docx')
```

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Пустой документ содержит один раздел, одно тело и один абзац.
# Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы,
# и получите узел документа без дочерних элементов.
doc.remove_all_children()
# В этом документе теперь нет составных дочерних узлов, к которым можно добавить содержимое.
# Если мы хотим его отредактировать, нам потребуется заново заполнить его коллекцию узлов.
# Сначала создайте новый раздел, а затем добавьте его как дочерний к корневому узлу документа.
section = aw.Section(doc)
doc.append_child(section)
# Установите некоторые свойства настройки страницы для раздела.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Разделу требуется тело, которое будет содержать и отображать всё его содержимое
# на странице между заголовком и нижним колонтитулом раздела.
body = aw.Body(doc)
section.append_child(body)
# Создайте абзац, задайте некоторые свойства форматирования и затем добавьте его как дочерний к телу.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Наконец, добавьте некоторое содержимое в документ. Создайте пробег,
# задать его внешний вид и содержимое, а затем добавить его как дочерний к абзацу.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

