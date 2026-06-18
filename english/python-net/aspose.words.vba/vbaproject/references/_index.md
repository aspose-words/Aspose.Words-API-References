---
title: VbaProject.references property
linktitle: references property
articleTitle: references property
second_title: Aspose.Words for Python
description: "VbaProject.references property. Gets a collection of VBA project references."
type: docs
weight: 70
url: /python-net/aspose.words.vba/vbaproject/references/
---

## VbaProject.references property

Gets a collection of VBA project references.


```python
@property
def references(self) -> aspose.words.vba.VbaReferenceCollection:
    ...

```

### Examples

Shows how to get/remove an element from the VBA reference collection (GetLibIdPath).

```python
@staticmethod
def _get_lib_id_path(reference):
    switch_condition = reference.type
    if switch_condition == aw.vba.VbaReferenceType.REGISTERED and switch_condition == aw.vba.VbaReferenceType.ORIGINAL and (switch_condition == aw.vba.VbaReferenceType.CONTROL):
        return ExVbaProject._get_lib_id_reference_path(reference.lib_id)
    elif switch_condition == aw.vba.VbaReferenceType.PROJECT:
        return ExVbaProject._get_lib_id_project_path(reference.lib_id)
    else:
        raise Exception()

@staticmethod
def _get_lib_id_reference_path(lib_id_reference):
    if lib_id_reference != None:
        ref_parts = lib_id_reference.split('#')
        if len(ref_parts) > 3:
            return ref_parts[3]
        return ''

@staticmethod
def _get_lib_id_project_path(lib_id_project):
    return libIdProject[3:] if libIdProject is not None else ''
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaProject](../)

