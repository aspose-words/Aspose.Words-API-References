---
title: VbaProject.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "VbaProject.name property. Gets or sets VBA project name."
type: docs
weight: 60
url: /de/python-net/aspose.words.vba/vbaproject/name/
---

## VbaProject.name property

Gets or sets VBA project name.


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
# Ein VBA-Projekt enthält eine Sammlung von Vba-Modulen.
vba_project = doc.vba_project
# Ermitteln Sie die Anzahl der VBA-Module mithilfe der count-Eigenschaft anstelle von len()
modules_count = vba_project.modules.count
print(f'Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n' if vba_project.is_signed else f'Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n')
vba_modules = doc.vba_project.modules
self.assertEqual(vba_modules.count, 3)
for module in vba_modules:
    print(f'Module name: {module.name};\nModule code:\n{module.source_code}\n')
# Setzen Sie neuen Quellcode für das VBA-Modul. Sie können auf VBA-Module in der Sammlung entweder über den Index oder über den Namen zugreifen.
vba_modules[0].source_code = 'Your VBA code...'
vba_modules.get_by_name('Module1').source_code = 'Your VBA code...'
# Entfernen Sie ein Modul aus der Sammlung.
vba_modules.remove(vba_modules[2])
```

Shows how to create a VBA project using macros.

```python
doc = aw.Document()
# Erstellen Sie ein neues VBA-Projekt.
project = aw.vba.VbaProject()
project.name = 'Aspose.Project'
doc.vba_project = project
# Erstellen Sie ein neues Modul und geben Sie den Makro-Quellcode an.
module = aw.vba.VbaModule()
module.name = 'Aspose.Module'
module.type = aw.vba.VbaModuleType.PROCEDURAL_MODULE
module.source_code = 'New source code'
# Fügen Sie das Modul dem VBA-Projekt hinzu.
doc.vba_project.modules.add(module)
doc.save(file_name=ARTIFACTS_DIR + 'VbaProject.CreateVBAMacros.docm')
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaProject](../)

