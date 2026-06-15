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


```python
@property
def lib_id(self) -> str:
    ...

```

### Remarks

Depending on reference type, the value of this property can be:

* a LibidReference specified at 2.1.1.8 LibidReference of [MS-OVBA]:
  https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
  
* a ProjectReference specified at 2.1.1.12 ProjectReference of [MS-OVBA]:
  https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131
  



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
* class [VbaReference](../)

