---
title: Aspose::Words::RevisionGroup::get_Text method
linktitle: get_Text
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::RevisionGroup::get_Text method. Returns inserted/deleted/moved text or description of format change in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/revisiongroup/get_text/
---
## RevisionGroup::get_Text method


Returns inserted/deleted/moved text or description of format change.

```cpp
System::String Aspose::Words::RevisionGroup::get_Text()
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

* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
