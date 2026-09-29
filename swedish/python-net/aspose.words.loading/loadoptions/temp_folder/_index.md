---
title: LoadOptions.temp_folder property
linktitle: temp_folder property
articleTitle: temp_folder property
second_title: Aspose.Words for Python
description: "LoadOptions.temp_folder property. Allows to use temporary files when reading document"
type: docs
weight: 160
url: /sv/python-net/aspose.words.loading/loadoptions/temp_folder/
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
# Observera att en sådan metod kan minska minnesanvändning men försämrar hastigheten
load_options = aw.loading.LoadOptions()
load_options.temp_folder = 'C:\\TempFolder\\'
# Säkerställ att katalogen finns och läs in
system_helper.io.Directory.create_directory(load_options.temp_folder)
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
```

Shows how to use the hard drive instead of memory when loading a document.

```python
# När vi läser in ett dokument lagras olika element tillfälligt i minnet medan sparoperationen pågår.
# Vi kan använda detta alternativ för att istället använda en temporär mapp i det lokala filsystemet,
# vilket kommer att minska vår applikations minnesbelastning.
options = aw.loading.LoadOptions()
options.temp_folder = ARTIFACTS_DIR + 'TempFiles'
# Den angivna temporära mappen måste finnas i det lokala filsystemet innan inläsningsoperationen.
system_helper.io.Directory.create_directory(options.temp_folder)
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=options)
# Mappen kommer att bestå utan återstående innehåll från inläsningsoperationen.
self.assertEqual(0, len(system_helper.io.Directory.get_files(options.temp_folder)))
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

