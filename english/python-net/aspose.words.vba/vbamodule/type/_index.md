---
title: VbaModule.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "VbaModule.type property. Specifies whether the module is a procedural module, document module, class module, or designer module."
type: docs
weight: 40
url: /python-net/aspose.words.vba/vbamodule/type/
---

## VbaModule.type property

Specifies whether the module is a procedural module, document module, class module, or designer module.


```python
@property
def type(self) -> aspose.words.vba.VbaModuleType:
    ...

@type.setter
def type(self, value: aspose.words.vba.VbaModuleType):
    ...

```

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
* class [VbaModule](../)

