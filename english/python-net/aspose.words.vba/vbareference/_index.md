---
title: VbaReference class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements a reference to an Automation type library or VBA project"
type: docs
weight: 50
url: /python-net/aspose.words.vba/vbareference/
---

## VbaReference class

Implements a reference to an Automation type library or VBA project.
To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/python-net/working-with-vba-macros/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [lib_id](./lib_id/) | Gets a string value containing the identifier of an Automation type library. |
| [type](./type/) | Gets [VbaReferenceType](../vbareferencetype/) object that indicates the type of reference that a [VbaReference](./) object represents. |

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

