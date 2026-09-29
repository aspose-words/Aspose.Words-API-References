---
title: VbaProject class
linktitle: VbaProject class
articleTitle: VbaProject class
second_title: Aspose.Words for Python
description: "aspose.words.vba.VbaProject class. Provides access to VBA project information"
type: docs
weight: 50
url: /es/python-net/aspose.words.vba/vbaproject/
---

## VbaProject class

Provides access to VBA project information.
A VBA project inside the document is defined as a collection of VBA modules.
To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/python-net/working-with-vba-macros/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [VbaProject()](./__init__/#default) | Creates a blank [VbaProject](./). |

### Properties

| Name | Description |
| --- | --- |
| [code_page](./code_page/) | Gets or sets the VBA project’s code page. |
| [is_protected](./is_protected/) | Shows whether the [VbaProject](./) is password protected. |
| [is_signed](./is_signed/) | Shows whether the [VbaProject](./) is signed or not. |
| [modules](./modules/) | Returns collection of VBA project modules. |
| [name](./name/) | Gets or sets VBA project name. |
| [references](./references/) | Gets a collection of VBA project references. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Performs a copy of the [VbaProject](./). |

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

* module [aspose.words.vba](../)

