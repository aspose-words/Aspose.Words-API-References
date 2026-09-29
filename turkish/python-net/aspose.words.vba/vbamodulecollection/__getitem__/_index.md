---
title: VbaModuleCollection indexer
linktitle: VbaModuleCollection indexer
articleTitle: VbaModuleCollection indexer
second_title: Aspose.Words for Python
description: "VbaModuleCollection indexer. Retrieves a [VbaModule](../../vbamodule/) object by index."
type: docs
weight: 10
url: /tr/python-net/aspose.words.vba/vbamodulecollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [VbaModule](../../vbamodule/) object by index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to access a document's VBA project information.

```python
from api_example_base import ApiExampleBase, MY_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'VBA project.docm')
# Bir VBA projesi, Vba modüllerinden oluşan bir koleksiyon içerir.
vba_project = doc.vba_project
# VBA modüllerinin sayısını len() yerine count özelliğiyle alın.
modules_count = vba_project.modules.count
print(f'Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n' if vba_project.is_signed else f'Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n')
vba_modules = doc.vba_project.modules
self.assertEqual(vba_modules.count, 3)
for module in vba_modules:
    print(f'Module name: {module.name};\nModule code:\n{module.source_code}\n')
# VBA modülü için yeni kaynak kodu ayarlayın. Koleksiyondaki VBA modüllerine indeks ya da ad ile erişebilirsiniz.
vba_modules[0].source_code = 'Your VBA code...'
vba_modules.get_by_name('Module1').source_code = 'Your VBA code...'
# Koleksiyondan bir modül kaldırın.
vba_modules.remove(vba_modules[2])
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaModuleCollection](../)

