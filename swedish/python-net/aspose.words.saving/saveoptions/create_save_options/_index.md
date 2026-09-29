---
title: SaveOptions.create_save_options method
linktitle: create_save_options method
articleTitle: create_save_options method
second_title: Aspose.Words for Python
description: "aspose.words.saving.SaveOptions.create_save_options method"
type: docs
weight: 210
url: /sv/python-net/aspose.words.saving/saveoptions/create_save_options/
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
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
save_options = aw.saving.SaveOptions.create_save_options(save_format=aw.SaveFormat.PDF)
# Ställ in egenskapen "MemoryOptimization" till "true" för att minska minnesavtrycket vid sparning av stora dokument
# på bekostnad av att förlänga operationens varaktighet.
# Ställ in egenskapen "MemoryOptimization" till "false" för att spara dokumentet som PDF normalt.
save_options.memory_optimization = memory_optimization
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.MemoryOptimization.pdf', save_options=save_options)
```

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# Aktivera automatisk stiluppdatering, men bifoga inte ett mall-dokument.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Eftersom det inte finns något mall-dokument hade dokumentet ingen plats att spåra stiländringar.
# Använd ett SaveOptions-objekt för att automatiskt ange en mall
# om ett dokument som vi sparar inte har en.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

## See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

