---
title: VbaModule.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "VbaModule.name property. Gets or sets VBA project module name."
type: docs
weight: 20
url: /it/python-net/aspose.words.vba/vbamodule/name/
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
# Un progetto VBA contiene una raccolta di moduli Vba.
vba_project = doc.vba_project
# Ottieni il conteggio dei moduli VBA usando la proprietà count invece di len()
modules_count = vba_project.modules.count
print(f'Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n' if vba_project.is_signed else f'Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n')
vba_modules = doc.vba_project.modules
self.assertEqual(vba_modules.count, 3)
for module in vba_modules:
    print(f'Module name: {module.name};\nModule code:\n{module.source_code}\n')
# Imposta nuovo codice sorgente per il modulo VBA. Puoi accedere ai moduli VBA nella raccolta sia per indice che per nome.
vba_modules[0].source_code = 'Your VBA code...'
vba_modules.get_by_name('Module1').source_code = 'Your VBA code...'
# Rimuovi un modulo dalla raccolta.
vba_modules.remove(vba_modules[2])
```

Shows how to create a VBA project using macros.

```python
doc = aw.Document()
# Crea un nuovo progetto VBA.
project = aw.vba.VbaProject()
project.name = 'Aspose.Project'
doc.vba_project = project
# Crea un nuovo modulo e specifica il codice sorgente della macro.
module = aw.vba.VbaModule()
module.name = 'Aspose.Module'
module.type = aw.vba.VbaModuleType.PROCEDURAL_MODULE
module.source_code = 'New source code'
# Aggiungi il modulo al progetto VBA.
doc.vba_project.modules.add(module)
doc.save(file_name=ARTIFACTS_DIR + 'VbaProject.CreateVBAMacros.docm')
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaModule](../)

