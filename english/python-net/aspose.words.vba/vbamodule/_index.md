﻿---
title: VbaModule class
linktitle: VbaModule class
articleTitle: VbaModule class
second_title: Aspose.Words for Python
description: "aspose.words.vba.VbaModule class. Provides access to VBA project module"
type: docs
weight: 20
url: /python-net/aspose.words.vba/vbamodule/
---

## VbaModule class

Provides access to VBA project module.
To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/python-net/working-with-vba-macros/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [VbaModule()](./__init__/#default) | Creates an empty module. |

### Properties

| Name | Description |
| --- | --- |
| [name](./name/) | Gets or sets VBA project module name. |
| [source_code](./source_code/) | Gets or sets VBA project module source code. |
| [type](./type/) | Specifies whether the module is a procedural module, document module, class module, or designer module. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Performs a copy of the [VbaModule](./). |

### Examples

Shows how to access a document's VBA project information.

```python
doc = aw.Document(MY_DIR + "VBA project.docm")

# A VBA project contains a collection of VBA modules.
vba_project = doc.vba_project
if vba_project.is_signed:
    print(f"Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {vba_project.modules.count}\n")
else:
    print(f"Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {vba_project.modules.count}\n")

vba_modules = doc.vba_project.modules

self.assertEqual(vba_modules.count, 3)

for module in vba_modules:
    print(f"Module name: {module.name};\nModule code:\n{module.source_code}\n")

# Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
vba_modules[0].source_code = "Your VBA code..."
vba_modules.get_by_name("Module1").source_code = "Your VBA code..."

# Remove a module from the collection.
vba_modules.remove(vba_modules[2])
```

### See Also

* module [aspose.words.vba](../)

