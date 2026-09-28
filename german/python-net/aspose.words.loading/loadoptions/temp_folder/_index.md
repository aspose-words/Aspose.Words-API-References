---
title: LoadOptions.temp_folder property
linktitle: temp_folder property
articleTitle: temp_folder property
second_title: Aspose.Words for Python
description: "LoadOptions.temp_folder property. Allows to use temporary files when reading document"
type: docs
weight: 160
url: /de/python-net/aspose.words.loading/loadoptions/temp_folder/
---

## LoadOptions.temp_folder property

Allows to use temporary files when reading document.
By default this property is ``None`` and no temporary files are used.



```python
@property
def temp_folder(self) -> str:
    ...

@temp_folder.setter
def temp_folder(self, value: str):
    ...

```

### Remarks

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when reading is complete.




### Examples

Shows how to load a document using temporary files.

```python
# Beachten Sie, dass ein solcher Ansatz den Speicherverbrauch reduzieren, aber die Geschwindigkeit verringern kann
load_options = aw.loading.LoadOptions()
load_options.temp_folder = 'C:\\TempFolder\\'
# Stellen Sie sicher, dass das Verzeichnis existiert und laden Sie
system_helper.io.Directory.create_directory(load_options.temp_folder)
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
```

Shows how to use the hard drive instead of memory when loading a document.

```python
# Wenn wir ein Dokument laden, werden verschiedene Elemente vorübergehend im Speicher abgelegt, während der Speichervorgang stattfindet.
# Wir können diese Option nutzen, um stattdessen einen temporären Ordner im lokalen Dateisystem zu verwenden,
# was den Speicheraufwand unserer Anwendung reduzieren wird.
options = aw.loading.LoadOptions()
options.temp_folder = ARTIFACTS_DIR + 'TempFiles'
# Der angegebene temporäre Ordner muss im lokalen Dateisystem existieren, bevor der Ladevorgang beginnt.
system_helper.io.Directory.create_directory(options.temp_folder)
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=options)
# Der Ordner bleibt erhalten, ohne Restinhalte aus dem Ladevorgang.
self.assertEqual(0, len(system_helper.io.Directory.get_files(options.temp_folder)))
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

