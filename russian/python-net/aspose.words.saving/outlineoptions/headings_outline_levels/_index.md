---
title: OutlineOptions.headings_outline_levels property
linktitle: headings_outline_levels property
articleTitle: headings_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.headings_outline_levels property. Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the  document outline."
type: docs
weight: 70
url: /ru/python-net/aspose.words.saving/outlineoptions/headings_outline_levels/
---

## OutlineOptions.headings_outline_levels property

Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the 
document outline.


```python
@property
def headings_outline_levels(self) -> int:
    ...

@headings_outline_levels.setter
def headings_outline_levels(self, value: int):
    ...

```

### Remarks

Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте заголовки уровней от 1 до 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Выходной PDF‑документ будет содержать оглавление, которое представляет собой таблицу содержания, перечисляющую заголовки в теле документа.
# Щелчок по элементу в этой структуре перенесёт нас к месту соответствующего заголовка.
# Установите свойство "HeadingsOutlineLevels" в "4", чтобы исключить из оглавления все заголовки уровней выше 4.
options.outline_options.headings_outline_levels = 4
# Если запись оглавления имеет последующие записи более высокого уровня между собой и следующей записью того же или более низкого уровня,
# слева от записи появится стрелка. Эта запись является "owner" нескольких таких "sub-entries".
# В нашем документе записи оглавления с пятого уровня заголовков являются подзаписями второй записи оглавления четвертого уровня,
# четвертый и пятый элементы уровней заголовков являются подэлементами второго элемента третьего уровня, и так далее.
# В структуре мы можем щёлкнуть по стрелке записи "owner", чтобы свернуть/развернуть все её подэлементы.
# Установите свойство "ExpandedOutlineLevels" в значение "2", чтобы автоматически раскрывать все элементы структуры уровня заголовка 2 и ниже
# и свернуть все элементы уровня 3 и выше при открытии документа.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

