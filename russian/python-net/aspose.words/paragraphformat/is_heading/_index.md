---
title: ParagraphFormat.is_heading property
linktitle: is_heading property
articleTitle: is_heading property
second_title: Aspose.Words for Python
description: "ParagraphFormat.is_heading property. True when the paragraph style is one of the built-in Heading styles."
type: docs
weight: 140
url: /ru/python-net/aspose.words/paragraphformat/is_heading/
---

## ParagraphFormat.is_heading property

True when the paragraph style is one of the built-in Heading styles.


```python
@property
def is_heading(self) -> bool:
    ...

```

### Examples

Shows how to limit the headings' level that will appear in the outline of a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте заголовки, которые могут служить элементами оглавления уровней 1, 2 и затем 3.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
save_options = aw.saving.PdfSaveOptions()
save_options.save_format = aw.SaveFormat.PDF
# Выходной PDF‑документ будет содержать оглавление, которое представляет собой таблицу содержания, перечисляющую заголовки в теле документа.
# Щелчок по элементу в этой структуре перенесёт нас к месту соответствующего заголовка.
# Установите свойство "HeadingsOutlineLevels" в значение "2", чтобы исключить из структуры все заголовки уровней выше 2.
# Последние два заголовка, которые мы вставили выше, не появятся.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeadingsOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

