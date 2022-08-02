---
title: clone method
second_title: Aspose.Words for Python via .NET API Reference
description: "Performs a copy of the [VbaProject](../)."
type: docs
weight: 70
url: /python-net/aspose.words.vba/vbaproject/clone/
---

## clone() {#default}

Performs a copy of the [VbaProject](../).



```python
def clone(self):
    ...
```

### Returns

The cloned VbaProject.


### Examples

Shows how to deep clone a VBA project and module.

```python
doc = aw.Document(MY_DIR + "VBA project.docm")
dest_doc = aw.Document()

copy_vba_project = doc.vba_project.clone()
dest_doc.vba_project = copy_vba_project

# In the destination document, we already have a module named "Module1"
# because we cloned it along with the project. We will need to remove the module.
old_vba_module = dest_doc.vba_project.modules.get_by_name("Module1")
copy_vba_module = doc.vba_project.modules.get_by_name("Module1").clone()
dest_doc.vba_project.modules.remove(old_vba_module)
dest_doc.vba_project.modules.add(copy_vba_module)

dest_doc.save(ARTIFACTS_DIR + "VbaProject.clone_vba_project.docm")
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaProject](../)

