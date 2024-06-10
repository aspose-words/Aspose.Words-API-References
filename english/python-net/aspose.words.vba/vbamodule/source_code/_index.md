---
title: VbaModule.source_code property
linktitle: source_code property
articleTitle: source_code property
second_title: Aspose.Words for Python
description: "VbaModule.source_code property. Gets or sets VBA project module source code."
type: docs
weight: 30
url: /python-net/aspose.words.vba/vbamodule/source_code/
---

## VbaModule.source_code property

Gets or sets VBA project module source code.


```python
@property
def source_code(self) -> str:
    ...

@source_code.setter
def source_code(self, value: str):
    ...

```

### Examples

Shows how to access a document's VBA project information.

```python
doc = aw.Document(MY_DIR + 'VBA project.docm')
# A VBA project contains a collection of VBA modules.
vba_project = doc.vba_project
if vba_project.is_signed:
    print(f'Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {vba_project.modules.count}\n')
else:
    print(f'Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {vba_project.modules.count}\n')
vba_modules = doc.vba_project.modules
self.assertEqual(vba_modules.count, 3)
for module in vba_modules:
    print(f'Module name: {module.name};\nModule code:\n{module.source_code}\n')
# Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
vba_modules[0].source_code = 'Your VBA code...'
vba_modules.get_by_name('Module1').source_code = 'Your VBA code...'
# Remove a module from the collection.
vba_modules.remove(vba_modules[2])
```

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

