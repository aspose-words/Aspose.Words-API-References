---
title: "Aspose::Words::RevisionGroup::get_RevisionType method"
linktitle: "get_RevisionType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::RevisionGroup::get_RevisionType method. Hämtar typen av revisioner som ingår i denna grupp i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/revisiongroup/get_revisiontype/
---
## RevisionGroup::get_RevisionType method


Hämtar typen av revisioner som ingår i denna grupp.

```cpp
Aspose::Words::RevisionType Aspose::Words::RevisionGroup::get_RevisionType()
```


## Exempel



Visar hur man skriver ut information om en grupp av revisioner i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```

## Se även

* Enum [RevisionType](../../revisiontype/)
* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
