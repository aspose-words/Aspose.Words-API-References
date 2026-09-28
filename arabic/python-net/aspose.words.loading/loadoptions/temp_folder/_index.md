---
title: LoadOptions.temp_folder property
linktitle: temp_folder property
articleTitle: temp_folder property
second_title: Aspose.Words for Python
description: "LoadOptions.temp_folder property. Allows to use temporary files when reading document"
type: docs
weight: 160
url: /ar/python-net/aspose.words.loading/loadoptions/temp_folder/
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
# لاحظ أن هذا النهج يمكن أن يقلل من استهلاك الذاكرة لكنه يبطئ السرعة
load_options = aw.loading.LoadOptions()
load_options.temp_folder = 'C:\\TempFolder\\'
# تأكد من وجود الدليل وحمّل
system_helper.io.Directory.create_directory(load_options.temp_folder)
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
```

Shows how to use the hard drive instead of memory when loading a document.

```python
# عند تحميل مستند، يتم تخزين عناصر مختلفة مؤقتًا في الذاكرة أثناء حدوث عملية الحفظ.
# يمكننا استخدام هذا الخيار لاستخدام مجلد مؤقت في نظام الملفات المحلي بدلاً من ذلك،
# مما سيقلل من استهلاك الذاكرة لتطبيقنا.
options = aw.loading.LoadOptions()
options.temp_folder = ARTIFACTS_DIR + 'TempFiles'
# يجب أن يكون المجلد المؤقت المحدد موجودًا في نظام الملفات المحلي قبل عملية التحميل.
system_helper.io.Directory.create_directory(options.temp_folder)
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=options)
# سوف يبقى المجلد موجودًا دون أي محتويات متبقية من عملية التحميل.
self.assertEqual(0, len(system_helper.io.Directory.get_files(options.temp_folder)))
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

