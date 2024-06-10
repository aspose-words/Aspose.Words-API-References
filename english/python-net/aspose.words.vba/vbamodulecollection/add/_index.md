---
title: VbaModuleCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "VbaModuleCollection.add method. Adds a module to the collection."
type: docs
weight: 30
url: /python-net/aspose.words.vba/vbamodulecollection/add/
---

## add(vba_module) {#vbamodule}

Adds a module to the collection.


```python
def add(self, vba_module: aspose.words.vba.VbaModule):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| vba_module | [VbaModule](../../vbamodule/) |  |

### Examples

Shows how to create a VBA project using macros.

```python
doc = aw.Document()
# Create a new VBA project.
project = aw.vba.VbaProject()
project.name = 'Aspose.Project'
doc.vba_project = project
# Create a new module and specify a macro source code.
module = aw.vba.VbaModule()
module.name = 'Aspose.Module'
module.type = aw.vba.VbaModuleType.PROCEDURAL_MODULE
module.source_code = 'New source code'
# Add the module to the VBA project.
doc.vba_project.modules.add(module)
doc.save(file_name=ARTIFACTS_DIR + 'VbaProject.CreateVBAMacros.docm')
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaModuleCollection](../)

