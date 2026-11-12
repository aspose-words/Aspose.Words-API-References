---
title: XpsSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 40
url: /ru/python-net/aspose.words.saving/xpssaveoptions/outline_options/
---

## XpsSaveOptions.outline_options property

Allows to specify outline options.


```python
@property
def outline_options(self) -> aspose.words.saving.OutlineOptions:
    ...

```

### Remarks

Note that [OutlineOptions.expanded_outline_levels](../../outlineoptions/expanded_outline_levels/) option will not work when saving to XPS.




### Examples

Shows how to limit the headings' level that will appear in the outline of a saved XPS document.

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
# Создайте объект "XpsSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод преобразует документ в .XPS.
save_options = aw.saving.XpsSaveOptions()
self.assertEqual(aw.SaveFormat.XPS, save_options.save_format)
# Выходной XPS‑документ будет содержать структуру, оглавление, в котором перечислены заголовки в теле документа.
# Щелчок по элементу в этой структуре перенесёт нас к месту соответствующего заголовка.
# Установите свойство "HeadingsOutlineLevels" в значение "2", чтобы исключить из структуры все заголовки уровней выше 2.
# Последние два заголовка, которые мы вставили выше, не появятся.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OutlineLevels.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

