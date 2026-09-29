---
title: VbaModule.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "VbaModule.name property. Gets or sets VBA project module name."
type: docs
weight: 20
url: /tr/python-net/aspose.words.vba/vbamodule/name/
---

## VbaModule.name property

Gets or sets VBA project module name.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

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

Shows how to create a VBA project using macros.

```python
doc = aw.Document()
# Yeni bir VBA projesi oluşturun.
project = aw.vba.VbaProject()
project.name = 'Aspose.Project'
doc.vba_project = project
# Yeni bir modül oluşturun ve bir makro kaynak kodu belirtin.
module = aw.vba.VbaModule()
module.name = 'Aspose.Module'
module.type = aw.vba.VbaModuleType.PROCEDURAL_MODULE
module.source_code = 'New source code'
# Modülü VBA projesine ekleyin.
doc.vba_project.modules.add(module)
doc.save(file_name=ARTIFACTS_DIR + 'VbaProject.CreateVBAMacros.docm')
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaModule](../)

