---
title: VbaModule constructor
linktitle: VbaModule constructor
articleTitle: VbaModule constructor
second_title: Aspose.Words for Python
description: "VbaModule constructor. Creates an empty module."
type: docs
weight: 10
url: /zh/python-net/aspose.words.vba/vbamodule/__init__/
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
* class [VbaModule](../)

