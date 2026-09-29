---
title: VbaModule.source_code property
linktitle: source_code property
articleTitle: source_code property
second_title: Aspose.Words for Python
description: "VbaModule.source_code property. Gets or sets VBA project module source code."
type: docs
weight: 30
url: /sv/python-net/aspose.words.vba/vbamodule/source_code/
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
from api_example_base import ApiExampleBase, MY_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'VBA project.docm')
# Ett VBA-projekt innehåller en samling av Vba-moduler.
vba_project = doc.vba_project
# Hämta antalet VBA-moduler med count-egenskapen istället för len()
modules_count = vba_project.modules.count
print(f'Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n' if vba_project.is_signed else f'Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n')
vba_modules = doc.vba_project.modules
self.assertEqual(vba_modules.count, 3)
for module in vba_modules:
    print(f'Module name: {module.name};\nModule code:\n{module.source_code}\n')
# Ange ny källkod för VBA-modulen. Du kan komma åt VBA-moduler i samlingen antingen via index eller namn.
vba_modules[0].source_code = 'Your VBA code...'
vba_modules.get_by_name('Module1').source_code = 'Your VBA code...'
# Ta bort en modul från samlingen.
vba_modules.remove(vba_modules[2])
```

Shows how to create a VBA project using macros.

```python
doc = aw.Document()
# Skapa ett nytt VBA-projekt.
project = aw.vba.VbaProject()
project.name = 'Aspose.Project'
doc.vba_project = project
# Skapa en ny modul och ange makrokällkoden.
module = aw.vba.VbaModule()
module.name = 'Aspose.Module'
module.type = aw.vba.VbaModuleType.PROCEDURAL_MODULE
module.source_code = 'New source code'
# Lägg till modulen i VBA-projektet.
doc.vba_project.modules.add(module)
doc.save(file_name=ARTIFACTS_DIR + 'VbaProject.CreateVBAMacros.docm')
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaModule](../)

