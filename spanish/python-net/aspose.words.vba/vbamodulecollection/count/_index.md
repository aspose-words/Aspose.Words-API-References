---
title: VbaModuleCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "VbaModuleCollection.count property. Returns the number of VBA modules in the collection."
type: docs
weight: 20
url: /es/python-net/aspose.words.vba/vbamodulecollection/count/
---

## VbaModuleCollection.count property

Returns the number of VBA modules in the collection.


```python
@property
def count(self) -> int:
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

### See Also

* module [aspose.words.vba](../../)
* class [VbaModuleCollection](../)

