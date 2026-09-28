---
title: VbaModuleCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "VbaModuleCollection.add method. Adds a module to the collection."
type: docs
weight: 30
url: /zh/python-net/aspose.words.vba/vbamodulecollection/add/
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
# 创建一个新的 VBA 项目。
project = aw.vba.VbaProject()
project.name = 'Aspose.Project'
doc.vba_project = project
# 创建一个新模块并指定宏源代码。
module = aw.vba.VbaModule()
module.name = 'Aspose.Module'
module.type = aw.vba.VbaModuleType.PROCEDURAL_MODULE
module.source_code = 'New source code'
# 将模块添加到 VBA 项目中。
doc.vba_project.modules.add(module)
doc.save(file_name=ARTIFACTS_DIR + 'VbaProject.CreateVBAMacros.docm')
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaModuleCollection](../)

