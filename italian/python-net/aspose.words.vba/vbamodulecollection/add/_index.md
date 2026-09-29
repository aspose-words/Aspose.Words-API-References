---
title: VbaModuleCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "VbaModuleCollection.add method. Adds a module to the collection."
type: docs
weight: 30
url: /it/python-net/aspose.words.vba/vbamodulecollection/add/
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
# Crea un nuovo progetto VBA.
project = aw.vba.VbaProject()
project.name = 'Aspose.Project'
doc.vba_project = project
# Crea un nuovo modulo e specifica il codice sorgente della macro.
module = aw.vba.VbaModule()
module.name = 'Aspose.Module'
module.type = aw.vba.VbaModuleType.PROCEDURAL_MODULE
module.source_code = 'New source code'
# Aggiungi il modulo al progetto VBA.
doc.vba_project.modules.add(module)
doc.save(file_name=ARTIFACTS_DIR + 'VbaProject.CreateVBAMacros.docm')
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaModuleCollection](../)

