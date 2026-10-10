---
title: OutlineOptions.create_missing_outline_levels property
linktitle: create_missing_outline_levels property
articleTitle: create_missing_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_missing_outline_levels property. Gets or sets a value determining whether or not to create missing outline levels when the document is  exported."
type: docs
weight: 30
url: /ru/python-net/aspose.words.saving/outlineoptions/create_missing_outline_levels/
---

## OutlineOptions.create_missing_outline_levels property

Gets or sets a value determining whether or not to create missing outline levels when the document is 
exported.

Default value for this property is ``False``.




```python
@property
def create_missing_outline_levels(self) -> bool:
    ...

@create_missing_outline_levels.setter
def create_missing_outline_levels(self, value: bool):
    ...

```

### Examples

Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте заголовки, которые могут служить элементами оглавления уровней 1 и 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.1.1.1.1')
builder.writeln('Heading 1.1.1.1.2')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
save_options = aw.saving.PdfSaveOptions()
# Выходной PDF‑документ будет содержать оглавление, которое представляет собой таблицу содержания, перечисляющую заголовки в теле документа.
# Щелчок по элементу в этой структуре перенесёт нас к месту соответствующего заголовка.
# Установите свойство "HeadingsOutlineLevels" в значение "5", чтобы включить в оглавление все заголовки уровней 5 и ниже.
save_options.outline_options.headings_outline_levels = 5
# Этот документ содержит заголовки уровней 1 и 5 и не содержит заголовков уровней 2, 3 и 4.
# Выходной PDF‑документ будет рассматривать уровни оглавления 2, 3 и 4 как "отсутствующие".
# Установите свойство "CreateMissingOutlineLevels" в значение "true", чтобы включить все отсутствующие уровни в оглавление,
# оставляя пустые элементы оглавления, поскольку нет пригодных заголовков.
# Установите свойство "CreateMissingOutlineLevels" в значение "false", чтобы игнорировать отсутствующие уровни оглавления,
# и рассматривать заголовки уровня 5 в оглавлении как уровень 2.
save_options.outline_options.create_missing_outline_levels = create_missing_outline_levels
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CreateMissingOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

