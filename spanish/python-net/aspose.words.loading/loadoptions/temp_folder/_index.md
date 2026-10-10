---
title: LoadOptions.temp_folder property
linktitle: temp_folder property
articleTitle: temp_folder property
second_title: Aspose.Words for Python
description: "LoadOptions.temp_folder property. Allows to use temporary files when reading document"
type: docs
weight: 160
url: /es/python-net/aspose.words.loading/loadoptions/temp_folder/
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
# Tenga en cuenta que este enfoque puede reducir el uso de memoria pero degrada la velocidad
load_options = aw.loading.LoadOptions()
load_options.temp_folder = 'C:\\TempFolder\\'
# Asegúrese de que el directorio exista y cargue
system_helper.io.Directory.create_directory(load_options.temp_folder)
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
```

Shows how to use the hard drive instead of memory when loading a document.

```python
# Cuando cargamos un documento, varios elementos se almacenan temporalmente en memoria mientras ocurre la operación de guardado.
# Podemos usar esta opción para utilizar una carpeta temporal en el sistema de archivos local en su lugar,
# lo que reducirá la sobrecarga de memoria de nuestra aplicación.
options = aw.loading.LoadOptions()
options.temp_folder = ARTIFACTS_DIR + 'TempFiles'
# La carpeta temporal especificada debe existir en el sistema de archivos local antes de la operación de carga.
system_helper.io.Directory.create_directory(options.temp_folder)
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=options)
# La carpeta permanecerá sin contenidos residuales de la operación de carga.
self.assertEqual(0, len(system_helper.io.Directory.get_files(options.temp_folder)))
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

