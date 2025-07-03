---
title: Aspose::Words::EditorType enum
linktitle: EditorType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EditorType enum. Specifies the set of possible aliases (or editing groups) which can be used as aliases to determine if the current user shall be allowed to edit a single range defined by an editable range within a document in C++.'
type: docs
weight: 88000
url: /cpp/aspose.words/editortype/
---
## EditorType enum


Specifies the set of possible aliases (or editing groups) which can be used as aliases to determine if the current user shall be allowed to edit a single range defined by an editable range within a document.

```cpp
enum class EditorType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Unspecified | 0 | Means that editor type is not specified. |
| Administrators | 1 | Specifies that users associated with the Administrators group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Contributors | 2 | Specifies that users associated with the Contributors group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Current | 3 | Specifies that users associated with the Current group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Editors | 4 | Specifies that users associated with the Editors group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Everyone | 5 | Specifies that all users that open the document shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| None | 6 | Specifies that none of the users that open the document shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Owners | 7 | Specifies that users associated with the Owners group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Default | n/a | Same as [Unspecified](./). |

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
