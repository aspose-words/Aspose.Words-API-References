---
title: VbaModule.source_code property
linktitle: source_code property
articleTitle: source_code property
second_title: Aspose.Words for Python
description: "VbaModule.source_code property. Gets or sets VBA project module source code."
type: docs
weight: 30
url: /es/python-net/aspose.words.vba/vbamodule/source_code/
---

## VbaModule.source_code property

Gets or sets VBA project module source code.


```python
@property
def source_code(self) -> str:
    ...

@source_code.setter
def source_code(self, value: str):
    ...

```

### Examples

Shows how to access a document's VBA project information.

```python
from api_example_base import ApiExampleBase, MY_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'VBA project.docm')
# Un proyecto VBA contiene una colección de módulos Vba.
vba_project = doc.vba_project
# Obtén el recuento de módulos VBA usando la propiedad count en lugar de len()
modules_count = vba_project.modules.count
print(f'Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n' if vba_project.is_signed else f'Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n')
vba_modules = doc.vba_project.modules
self.assertEqual(vba_modules.count, 3)
for module in vba_modules:
    print(f'Module name: {module.name};\nModule code:\n{module.source_code}\n')
# Establece nuevo código fuente para el módulo VBA. Puedes acceder a los módulos VBA en la colección ya sea por índice o por nombre.
vba_modules[0].source_code = 'Your VBA code...'
vba_modules.get_by_name('Module1').source_code = 'Your VBA code...'
# Elimina un módulo de la colección.
vba_modules.remove(vba_modules[2])
```

Shows how to create a VBA project using macros.

```python
doc = aw.Document()
# Crea un nuevo proyecto VBA.
project = aw.vba.VbaProject()
project.name = 'Aspose.Project'
doc.vba_project = project
# Crea un nuevo módulo y especifica el código fuente de la macro.
module = aw.vba.VbaModule()
module.name = 'Aspose.Module'
module.type = aw.vba.VbaModuleType.PROCEDURAL_MODULE
module.source_code = 'New source code'
# Agrega el módulo al proyecto VBA.
doc.vba_project.modules.add(module)
doc.save(file_name=ARTIFACTS_DIR + 'VbaProject.CreateVBAMacros.docm')
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaModule](../)

