---
title: UnlinkFields
second_title: Aspose.Words for C++ API Reference
description: Unlinks fields in the whole document.
type: docs
weight: 1158
url: /cpp/aspose.words/document/unlinkfields/
---
## Document::UnlinkFields method


Unlinks fields in the whole document.

```cpp
void Aspose::Words::Document::UnlinkFields()
```

## Remarks


Replaces all the fields in the whole document with their most recent results.

To unlink fields in a specific part of the document use [UnlinkFields](../../range/unlinkfields/).

## Examples



Shows how to unlink all fields in the document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Linked fields.docx");

doc->UnlinkFields();
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
