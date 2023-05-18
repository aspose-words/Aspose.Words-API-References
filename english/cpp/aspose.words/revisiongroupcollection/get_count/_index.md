---
title: Aspose::Words::RevisionGroupCollection::get_Count method
linktitle: get_Count
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::RevisionGroupCollection::get_Count method. Returns the number of revision groups in the collection in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/revisiongroupcollection/get_count/
---
## RevisionGroupCollection::get_Count method


Returns the number of revision groups in the collection.

```cpp
int32_t Aspose::Words::RevisionGroupCollection::get_Count()
```


## Examples



Shows how to print info about a group of revisions in a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (const auto& group : doc->get_Revisions()->get_Groups())
{
    std::cout << String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(),
                                group->get_Text())
              << std::endl;
}
```

## See Also

* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
