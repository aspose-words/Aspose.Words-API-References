---
title: VbaModule.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "VbaModule.name property. Gets or sets VBA project module name."
type: docs
weight: 20
url: /zh/python-net/aspose.words.vba/vbamodule/name/
---

## VbaModule.name property

Gets or sets VBA project module name.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

### Examples

Shows how to access a document's VBA project information.

```python
from api_example_base import ApiExampleBase, MY_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'VBA project.docm')
# VBA 项目包含一组 Vba 模块。
vba_project = doc.vba_project
# 使用 count 属性而不是 len() 获取 VBA 模块的数量。
modules_count = vba_project.modules.count
print(f'Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n' if vba_project.is_signed else f'Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n')
vba_modules = doc.vba_project.modules
self.assertEqual(vba_modules.count, 3)
for module in vba_modules:
    print(f'Module name: {module.name};\nModule code:\n{module.source_code}\n')
# 为 VBA 模块设置新的源代码。您可以通过索引或名称访问集合中的 VBA 模块。
vba_modules[0].source_code = 'Your VBA code...'
vba_modules.get_by_name('Module1').source_code = 'Your VBA code...'
# 从集合中移除一个模块。
vba_modules.remove(vba_modules[2])
```

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

