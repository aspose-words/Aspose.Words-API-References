---
title: VbaReference.lib_id property
linktitle: lib_id property
articleTitle: lib_id property
second_title: Aspose.Words for Python
description: "VbaReference.lib_id property. Gets a string value containing the identifier of an Automation type library."
type: docs
weight: 10
url: /python-net/aspose.words.vba/vbareference/lib_id/
---

## VbaReference.lib_id property

Gets a string value containing the identifier of an Automation type library.

Depending on reference type, the value of this property can be:

* a LibidReference specified at 2.1.1.8 LibidReference of [MS-OVBA]:
  https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
  
* a ProjectReference specified at 2.1.1.12 ProjectReference of [MS-OVBA]:
  https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131
  



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

* module [aspose.words.vba](../../)
* class [VbaReference](../)

