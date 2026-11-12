---
title: SaveOptions.create_save_options method
linktitle: create_save_options method
articleTitle: create_save_options method
second_title: Aspose.Words for Python
description: "aspose.words.saving.SaveOptions.create_save_options method"
type: docs
weight: 210
url: /ru/python-net/aspose.words.saving/saveoptions/create_save_options/
---

## create_save_options(save_format) {#saveformat}

Creates a save options object of a class suitable for the specified save format.


```python
def create_save_options(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format for which to create a save options object. |

### Returns

An object of a class that derives from [SaveOptions](../).


## create_save_options(file_name) {#str}

Creates a save options object of a class suitable for the file extension specified in the given file name.


```python
def create_save_options(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The extension of this file name determines the class of the save options object to create. |

### Returns

An object of a class that derives from [SaveOptions](../).


## Examples

Shows an option to optimize memory consumption when rendering large documents to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
save_options = aw.saving.SaveOptions.create_save_options(save_format=aw.SaveFormat.PDF)
# Установите свойство "MemoryOptimization" в значение "true", чтобы уменьшить объём памяти, используемый при сохранении больших документов
# ценой увеличения длительности операции.
# Установите свойство "MemoryOptimization" в значение "false", чтобы сохранять документ как PDF в обычном режиме.
save_options.memory_optimization = memory_optimization
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.MemoryOptimization.pdf', save_options=save_options)
```

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# Включите автоматическое обновление стилей, но не прикрепляйте шаблонный документ.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Поскольку шаблонного документа нет, у документа не было места для отслеживания изменений стилей.
# Используйте объект SaveOptions для автоматической установки шаблона
# если сохраняемый документ не имеет его.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

## See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

