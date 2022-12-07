---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Returns a revision group at the specified index.
type: docs
weight: 105
url: /cpp/aspose.words/revisiongroupcollection/idx_get/
---
## RevisionGroupCollection::idx_get method


Returns a revision group at the specified index.

```cpp
System::SharedPtr<Aspose::Words::RevisionGroup> Aspose::Words::RevisionGroupCollection::idx_get(int32_t index)
```


## Examples



Shows how to get a group of revisions in a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Revisions.docx");

SharedPtr<RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## See Also

* Class [RevisionGroup](../../revisiongroup/)
* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
