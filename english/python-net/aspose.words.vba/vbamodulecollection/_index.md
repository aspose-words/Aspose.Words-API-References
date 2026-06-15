---
title: VbaModuleCollection class
linktitle: VbaModuleCollection class
articleTitle: VbaModuleCollection class
second_title: Aspose.Words for Python
description: "aspose.words.vba.VbaModuleCollection class. Represents a collection of [VbaModule](../vbamodule/) objects"
type: docs
weight: 30
url: /python-net/aspose.words.vba/vbamodulecollection/
---

## VbaModuleCollection class

Represents a collection of [VbaModule](../vbamodule/) objects.
To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/python-net/working-with-vba-macros/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [VbaModule](../vbamodule/) object by index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of VBA modules in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(vba_module)](./add/#vbamodule) | Adds a module to the collection. |
|[ get_by_name(name)](./get_by_name/#str) | Retrieves a [VbaModule](../vbamodule/) object by name, or Null if not found. |
|[ remove(module)](./remove/#vbamodule) | Removes the specified module from the collection. |

### Examples

Shows how to access a document's VBA project information.

```python
from api_example_base import ApiExampleBase, MY_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'VBA project.docm')
# A VBA project contains a collection of Vba modules.
vba_project = doc.vba_project
# Get the count of VBA modules using count property instead of len()
modules_count = vba_project.modules.count
print(f'Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n' if vba_project.is_signed else f'Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n')
vba_modules = doc.vba_project.modules
self.assertEqual(vba_modules.count, 3)
for module in vba_modules:
    print(f'Module name: {module.name};\nModule code:\n{module.source_code}\n')
# Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
vba_modules[0].source_code = 'Your VBA code...'
vba_modules.get_by_name('Module1').source_code = 'Your VBA code...'
# Remove a module from the collection.
vba_modules.remove(vba_modules[2])
```

### See Also

* module [aspose.words.vba](../)

