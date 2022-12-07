---
title: get_Author
second_title: Aspose.Words for C++ API Reference
description: Gets the author of this revision group.
type: docs
weight: 14
url: /cpp/aspose.words/revisiongroup/get_author/
---
## RevisionGroup::get_Author method


Gets the author of this revision group.

```cpp
System::String Aspose::Words::RevisionGroup::get_Author()
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
* Library [Aspose.Words](../../../)
