---
title: LoadOptions.temp_folder property
linktitle: temp_folder property
articleTitle: temp_folder property
second_title: Aspose.Words for Python
description: "LoadOptions.temp_folder property. Allows to use temporary files when reading document"
type: docs
weight: 160
url: /zh/python-net/aspose.words.loading/loadoptions/temp_folder/
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
# 请注意，此类做法可以降低内存使用，但会降低速度。
load_options = aw.loading.LoadOptions()
load_options.temp_folder = 'C:\\TempFolder\\'
# 确保目录存在并加载
system_helper.io.Directory.create_directory(load_options.temp_folder)
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
```

Shows how to use the hard drive instead of memory when loading a document.

```python
# 当我们加载文档时，各种元素会在保存操作进行时暂时存储在内存中。
# 我们可以使用此选项改为在本地文件系统中使用临时文件夹，
# 这将降低我们应用程序的内存开销。
options = aw.loading.LoadOptions()
options.temp_folder = ARTIFACTS_DIR + 'TempFiles'
# 指定的临时文件夹必须在加载操作之前已存在于本地文件系统中。
system_helper.io.Directory.create_directory(options.temp_folder)
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=options)
# 文件夹将在加载操作后保持存在，并且没有残留内容。
self.assertEqual(0, len(system_helper.io.Directory.get_files(options.temp_folder)))
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

