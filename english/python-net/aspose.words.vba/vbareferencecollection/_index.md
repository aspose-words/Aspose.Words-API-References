---
title: VbaReferenceCollection class
linktitle: VbaReferenceCollection class
articleTitle: VbaReferenceCollection class
second_title: Aspose.Words for Python
description: "aspose.words.vba.VbaReferenceCollection class. Represents a collection of [VbaReference](../vbareference/) objects"
type: docs
weight: 70
url: /python-net/aspose.words.vba/vbareferencecollection/
---

## VbaReferenceCollection class

Represents a collection of [VbaReference](../vbareference/) objects.
To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/python-net/working-with-vba-macros/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets [VbaReference](../vbareference/) object at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of VBA references in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ remove(item)](./remove/#vbareference) | Removes the first occurrence of a specified [VbaReference](../vbareference/) item from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes the [VbaReference](../vbareference/) element at the specified index of the collection. |

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

* module [aspose.words.vba](../)

