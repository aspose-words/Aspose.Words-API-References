---
title: SaveOptions.temp_folder property
linktitle: temp_folder property
articleTitle: temp_folder property
second_title: Aspose.Words for Python
description: "SaveOptions.temp_folder property. Specifies the folder for temporary files used when saving to a DOC or DOCX file"
type: docs
weight: 120
url: /fr/python-net/aspose.words.saving/saveoptions/temp_folder/
---

## SaveOptions.temp_folder property

Specifies the folder for temporary files used when saving to a DOC or DOCX file.
By default, this property is ``None`` and no temporary files are used.



```python
@property
def temp_folder(self) -> str:
    ...

@temp_folder.setter
def temp_folder(self, value: str):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(OutOfMemoryException)) | Throw if you are saving a very large document (thousands of pages) and/or processing many documents at the same time. The memory spike during saving can be significant enough to cause the exception. |

### Remarks

When Aspose.Words saves a document, it needs to create temporary internal structures. By default,
these internal structures are created in memory and the memory usage spikes for a short period while
the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

Specifying a temporary folder using [SaveOptions.temp_folder](./) will cause Aspose.Words to keep the internal structures in
temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.




### Examples

Shows how to use the hard drive instead of memory when saving a document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Lorsque nous enregistrons un document, divers éléments sont temporairement stockés en mémoire pendant que l'opération d'enregistrement se déroule.
# Nous pouvons utiliser cette option pour employer un dossier temporaire sur le système de fichiers local à la place,
# ce qui réduira la charge mémoire de notre application.
options = aw.saving.DocSaveOptions()
options.temp_folder = ARTIFACTS_DIR + 'TempFiles'
# Le dossier temporaire spécifié doit exister dans le système de fichiers local avant l'opération d'enregistrement.
system_helper.io.Directory.create_directory(options.temp_folder)
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.TempFolder.doc', save_options=options)
# Le dossier persistera sans aucun contenu résiduel provenant de l'opération de chargement.
self.assertEqual(0, len(system_helper.io.Directory.get_files(options.temp_folder)))
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

