---
title: PageSetup.restart_page_numbering property
linktitle: restart_page_numbering property
articleTitle: restart_page_numbering property
second_title: Aspose.Words for Python
description: "PageSetup.restart_page_numbering property. True if page numbering restarts at the beginning of the section."
type: docs
weight: 360
url: /ru/python-net/aspose.words/pagesetup/restart_page_numbering/
---

## PageSetup.restart_page_numbering property

True if page numbering restarts at the beginning of the section.


```python
@property
def restart_page_numbering(self) -> bool:
    ...

@restart_page_numbering.setter
def restart_page_numbering(self, value: bool):
    ...

```

### Remarks

If set to ``False``, the [PageSetup.restart_page_numbering](./) property will override the
[PageSetup.page_starting_number](../page_starting_number/) property so that page numbering can continue from the previous section.



### Examples

Shows how to set up page numbering in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 3.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('Section 2, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 3.')
# Переместите построитель документа в основной header первого раздела,
# который будет отображаться на каждой странице этого раздела.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
# Вставьте поле PAGE, которое будет отображать номер текущей страницы.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
# Настройте раздел так, чтобы нумерация, отображаемая полями PAGE, начиналась с 5.
# Также настройте все поля PAGE так, чтобы они отображали номера страниц римскими цифрами верхнего регистра.
page_setup = doc.sections[0].page_setup
page_setup.restart_page_numbering = True
page_setup.page_starting_number = 5
page_setup.page_number_style = aw.NumberStyle.UPPERCASE_ROMAN
# Создайте еще один основной header для второго раздела с еще одним полем PAGE.
builder.move_to_section(1)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.write(' - ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' - ')
# Настройте раздел так, чтобы нумерация, отображаемая полями PAGE, начиналась с 10.
# Также настройте все поля PAGE так, чтобы они отображали номера страниц арабскими цифрами.
page_setup = doc.sections[1].page_setup
page_setup.page_starting_number = 10
page_setup.restart_page_numbering = True
page_setup.page_number_style = aw.NumberStyle.ARABIC
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageNumbering.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

