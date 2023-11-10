---
title: VbaModuleCollection indexer
linktitle: VbaModuleCollection indexer
articleTitle: VbaModuleCollection indexer
second_title: Aspose.Words for Python
description: "VbaModuleCollection indexer. Retrieves a [VbaModule](../../vbamodule/) object by index."
type: docs
weight: 10
url: /python-net/aspose.words.vba/vbamodulecollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [VbaModule](../../vbamodule/) object by index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the module to retrieve. |

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

* module [aspose.words.vba](../../)
* class [VbaModuleCollection](../)

