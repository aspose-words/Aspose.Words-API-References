﻿---
title: VbaModule constructor
linktitle: VbaModule constructor
articleTitle: VbaModule constructor
second_title: Aspose.Words for Python
description: "VbaModule constructor. Creates an empty module."
type: docs
weight: 10
url: /python-net/aspose.words.vba/vbamodule/__init__/
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

