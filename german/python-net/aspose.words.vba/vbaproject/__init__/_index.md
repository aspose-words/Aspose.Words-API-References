---
title: VbaProject constructor
linktitle: VbaProject constructor
articleTitle: VbaProject constructor
second_title: Aspose.Words for Python
description: "VbaProject constructor. Creates a blank [VbaProject](../)."
type: docs
weight: 10
url: /de/python-net/aspose.words.vba/vbaproject/__init__/
---

## VbaProject() {#default}

Creates a blank [VbaProject](../).



```python
def __init__(self):
    ...
```

### Examples

Shows how to create a VBA project using macros.

```python
doc = aw.Document()
# Erstellen Sie ein neues VBA-Projekt.
project = aw.vba.VbaProject()
project.name = 'Aspose.Project'
doc.vba_project = project
# Erstellen Sie ein neues Modul und geben Sie den Makro-Quellcode an.
module = aw.vba.VbaModule()
module.name = 'Aspose.Module'
module.type = aw.vba.VbaModuleType.PROCEDURAL_MODULE
module.source_code = 'New source code'
# Fügen Sie das Modul dem VBA-Projekt hinzu.
doc.vba_project.modules.add(module)
doc.save(file_name=ARTIFACTS_DIR + 'VbaProject.CreateVBAMacros.docm')
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaProject](../)

