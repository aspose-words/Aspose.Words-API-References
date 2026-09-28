---
title: VbaProject.modules property
linktitle: modules property
articleTitle: modules property
second_title: Aspose.Words for Python
description: "VbaProject.modules property. Returns collection of VBA project modules."
type: docs
weight: 50
url: /ar/python-net/aspose.words.vba/vbaproject/modules/
---

## VbaProject.modules property

Returns collection of VBA project modules.


```python
@property
def modules(self) -> aspose.words.vba.VbaModuleCollection:
    ...

```

### Examples

Shows how to access a document's VBA project information.

```python
from api_example_base import ApiExampleBase, MY_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'VBA project.docm')
# يحتوي مشروع VBA على مجموعة من وحدات Vba.
vba_project = doc.vba_project
# احصل على عدد وحدات VBA باستخدام خاصية count بدلاً من len()
modules_count = vba_project.modules.count
print(f'Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n' if vba_project.is_signed else f'Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n')
vba_modules = doc.vba_project.modules
self.assertEqual(vba_modules.count, 3)
for module in vba_modules:
    print(f'Module name: {module.name};\nModule code:\n{module.source_code}\n')
# عيّن شفرة مصدر جديدة لوحدة VBA. يمكنك الوصول إلى وحدات VBA في المجموعة إما بالفهرس أو بالاسم.
vba_modules[0].source_code = 'Your VBA code...'
vba_modules.get_by_name('Module1').source_code = 'Your VBA code...'
# أزل وحدة من المجموعة.
vba_modules.remove(vba_modules[2])
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaProject](../)

