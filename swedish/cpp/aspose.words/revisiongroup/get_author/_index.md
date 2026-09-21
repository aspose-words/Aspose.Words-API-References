---
title: "Aspose::Words::RevisionGroup::get_Author method"
linktitle: "get_Author"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::RevisionGroup::get_Author metod. Hämtar författaren till den här revisionsgruppen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/revisiongroup/get_author/
---
## RevisionGroup::get_Author method


Hämtar författaren till denna revisionsgrupp.

```cpp
System::String Aspose::Words::RevisionGroup::get_Author()
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

* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
