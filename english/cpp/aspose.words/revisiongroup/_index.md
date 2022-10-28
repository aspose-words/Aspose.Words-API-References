---
title: RevisionGroup
second_title: Aspose.Words for C++ API Reference
description: Represents a group of sequential Revision objects.
type: docs
weight: 690
url: /cpp/aspose.words/revisiongroup/
---
## RevisionGroup class


Represents a group of sequential [Revision](../revision/) objects.

```cpp
class RevisionGroup : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Author](./get_author/)() | Gets the author of this revision group. |
| [get_RevisionType](./get_revisiontype/)() | Gets the type of revisions included in this group. |
| [get_Text](./get_text/)() | Returns inserted/deleted/moved text or description of format change. |

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

