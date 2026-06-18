---
title: VbaReferenceCollection indexer
linktitle: VbaReferenceCollection indexer
articleTitle: VbaReferenceCollection indexer
second_title: Aspose.Words for Python
description: "VbaReferenceCollection indexer. Gets [VbaReference](../../vbareference/) object at the specified index."
type: docs
weight: 10
url: /python-net/aspose.words.vba/vbareferencecollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets [VbaReference](../../vbareference/) object at the specified index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

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
* class [VbaReferenceCollection](../)

