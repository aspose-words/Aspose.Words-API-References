---
title: VbaProject.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Python
description: "VbaProject.clone method. Performs a copy of the [VbaProject](../)."
type: docs
weight: 80
url: /zh/python-net/aspose.words.vba/vbaproject/clone/
---

## clone() {#default}

Performs a copy of the [VbaProject](../).



```python
def clone(self):
    ...
```

### Returns

The cloned [VbaProject](../).


### Examples

Shows how to deep clone a VBA project and module.

```python
doc = aw.Document(file_name=MY_DIR + 'VBA project.docm')
dest_doc = aw.Document()
copy_vba_project = doc.vba_project.clone()
dest_doc.vba_project = copy_vba_project
# 在目标文档中，我们已经有一个名为 "Module1" 的模块
# 因为我们连同项目一起克隆了它。我们需要移除该模块。
old_vba_module = dest_doc.vba_project.modules.get_by_name('Module1')
copy_vba_module = doc.vba_project.modules.get_by_name('Module1').clone()
dest_doc.vba_project.modules.remove(old_vba_module)
dest_doc.vba_project.modules.add(copy_vba_module)
dest_doc.save(file_name=ARTIFACTS_DIR + 'VbaProject.CloneVbaProject.docm')
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaProject](../)

