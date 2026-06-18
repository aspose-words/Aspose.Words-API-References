---
title: VbaReferenceCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "VbaReferenceCollection.remove method. Removes the first occurrence of a specified [VbaReference](../../vbareference/) item from the collection."
type: docs
weight: 30
url: /python-net/aspose.words.vba/vbareferencecollection/remove/
---

## remove(item) {#vbareference}

Removes the first occurrence of a specified [VbaReference](../../vbareference/) item from the collection. 



```python
def remove(self, item: aspose.words.vba.VbaReference):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| item | [VbaReference](../../vbareference/) |  |

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

