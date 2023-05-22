﻿---
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

Shows how to get/remove an element from the VBA reference collection.

```python
def test_remove_vba_reference(self):

    broken_path = r"X:\broken.dll"
    doc = aw.Document(MY_DIR + "VBA project.docm")

    references = doc.vba_project.references
    self.assertEqual(5, references.count)

    for i in range(references.count):

        reference = doc.vba_project.references[i]
        path = self.get_lib_id_path(reference)

        if path == broken_path:
            references.remove_at(i)

    self.assertEqual(4, references.count)

    references.remove(references[1])
    self.assertEqual(3, references.count)

    doc.save(ARTIFACTS_DIR + "VbaProject.remove_vba_reference.docm")

def get_lib_id_path(self, reference: aw.vba.VbaReference) -> str:
    """Returns string representing LibId path of a specified reference."""

    if reference.type in (aw.vba.VbaReferenceType.REGISTERED,
                          aw.vba.VbaReferenceType.ORIGINAL,
                          aw.vba.VbaReferenceType.CONTROL):
        return self.get_lib_id_reference_path(reference.lib_id)

    if reference.type == aw.vba.VbaReferenceType.PROJECT:
        return self.get_lib_id_project_path(reference.lib_id)

    raise ValueError()

def get_lib_id_reference_path(self, lib_id_reference: str) -> str:
    """Returns path from a specified identifier of an Automation type library."""

    if lib_id_reference is not None:
        ref_parts = lib_id_reference.split('#')
        if len(ref_parts) > 3:
            return ref_parts[3]

    return ""

def get_lib_id_project_path(self, lib_id_project: str) -> str:
    """Returns path from a specified identifier of an Automation type library."""

    return lib_id_project[3:] if lib_id_project is not None else ""
```

### See Also

* module [aspose.words.vba](../)

