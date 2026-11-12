---
title: FixedPageSaveOptions.optimize_output property
linktitle: optimize_output property
articleTitle: optimize_output property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.optimize_output property. Flag indicates whether it is required to optimize output"
type: docs
weight: 50
url: /ru/python-net/aspose.words.saving/fixedpagesaveoptions/optimize_output/
---

## FixedPageSaveOptions.optimize_output property

Flag indicates whether it is required to optimize output.
If this flag is set redundant nested canvases and empty canvases are removed,
also neighbor glyphs with the same formatting are concatenated.
Note: The accuracy of the content display may be affected if this property is set to ``True``.

Default is ``False``.



```python
@property
def optimize_output(self) -> bool:
    ...

@optimize_output.setter
def optimize_output(self, value: bool):
    ...

```

### Examples

Shows how to optimize document objects while saving to xps.

```python
doc = aw.Document(file_name=MY_DIR + 'Unoptimized document.docx')
# Создайте объект "XpsSaveOptions", чтобы передать его методу "Save" документа
# чтобы изменить способ, которым этот метод преобразует документ в .XPS.
save_options = aw.saving.XpsSaveOptions()
# Установите свойство "OptimizeOutput" в значение "true", чтобы принять меры, такие как удаление вложенных или пустых холстов
# и объединение соседних фрагментов с одинаковым форматированием для оптимизации содержимого выходного документа.
# Это может повлиять на внешний вид документа.
# Установите свойство "OptimizeOutput" в значение "false", чтобы сохранить документ обычным способом.
save_options.optimize_output = optimize_output
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OptimizeOutput.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

