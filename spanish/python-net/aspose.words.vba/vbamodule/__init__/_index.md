---
title: VbaModule constructor
linktitle: VbaModule constructor
articleTitle: VbaModule constructor
second_title: Aspose.Words for Python
description: "VbaModule constructor. Creates an empty module."
type: docs
weight: 10
url: /es/python-net/aspose.words.vba/vbamodule/__init__/
---

## VbaModule() {#default}

Creates an empty module.


```python
def __init__(self):
    ...
```

### Examples

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

