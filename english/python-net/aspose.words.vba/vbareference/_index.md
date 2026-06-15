---
title: VbaReference class
linktitle: VbaReference class
articleTitle: VbaReference class
second_title: Aspose.Words for Python
description: "aspose.words.vba.VbaReference class. Implements a reference to an Automation type library or VBA project"
type: docs
weight: 60
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

