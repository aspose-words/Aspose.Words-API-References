---
title: temp_folder property
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to use temporary files when reading document"
type: docs
weight: 140
url: /python-net/aspose.words.loading/loadoptions/temp_folder/
---

## LoadOptions.temp_folder property

Allows to use temporary files when reading document.
By default this property is ``None`` and no temporary files are used.


The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when reading is complete.




### Examples

Shows how to load a document using temporary files.

```python
# Note that such an approach can reduce memory usage but degrades speed
load_options = aw.loading.LoadOptions()
load_options.temp_folder = "C:\\TempFolder\\"

# Ensure that the directory exists and load
os.makedirs(load_options.temp_folder, exist_ok=True)

doc = aw.Document(MY_DIR + "Document.docx", load_options)
```

Shows how to use the hard drive instead of memory when loading a document.

```python
# When we load a document, various elements are temporarily stored in memory as the save operation occurs.
# We can use this option to use a temporary folder in the local file system instead,
# which will reduce our application's memory overhead.
options = aw.loading.LoadOptions()
options.temp_folder = ARTIFACTS_DIR + "TempFiles"

# The specified temporary folder must exist in the local file system before the load operation.
os.makedirs(options.temp_folder, exist_ok=True)

doc = aw.Document(MY_DIR + "Document.docx", options)

# The folder will persist with no residual contents from the load operation.
self.assertListEqual([], os.listdir(options.temp_folder))
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

