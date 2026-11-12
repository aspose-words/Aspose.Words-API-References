---
title: VbaProject.code_page property
linktitle: code_page property
articleTitle: code_page property
second_title: Aspose.Words for Python
description: "VbaProject.code_page property. Gets or sets the VBA project’s code page."
type: docs
weight: 20
url: /ru/python-net/aspose.words.vba/vbaproject/code_page/
---

## VbaProject.code_page property

Gets or sets the VBA project’s code page.


```python
@property
def code_page(self) -> int:
    ...

@code_page.setter
def code_page(self, value: int):
    ...

```

### Remarks

Please note that VBA is pre-Unicode feature and you have to explicitly set appropriate code page
to preserve regional character sets.


### Examples

Shows how to access a document's VBA project information.

```python
from api_example_base import ApiExampleBase, MY_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'VBA project.docm')
# Проект VBA содержит коллекцию модулей Vba.
vba_project = doc.vba_project
# Получите количество модулей VBA, используя свойство count вместо len()
modules_count = vba_project.modules.count
print(f'Project name: {vba_project.name} signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n' if vba_project.is_signed else f'Project name: {vba_project.name} not signed; Project code page: {vba_project.code_page}; Modules count: {modules_count}\n')
vba_modules = doc.vba_project.modules
self.assertEqual(vba_modules.count, 3)
for module in vba_modules:
    print(f'Module name: {module.name};\nModule code:\n{module.source_code}\n')
# Установите новый исходный код для модуля VBA. Вы можете получить доступ к модулям VBA в коллекции либо по индексу, либо по имени.
vba_modules[0].source_code = 'Your VBA code...'
vba_modules.get_by_name('Module1').source_code = 'Your VBA code...'
# Удалите модуль из коллекции.
vba_modules.remove(vba_modules[2])
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaProject](../)

