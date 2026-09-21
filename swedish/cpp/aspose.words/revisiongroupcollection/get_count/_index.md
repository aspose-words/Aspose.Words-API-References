---
title: "Aspose::Words::RevisionGroupCollection::get_Count-metoden"
linktitle: "get_Count"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::RevisionGroupCollection::get_Count-metoden. Returnerar antalet revisionsgrupper i samlingen i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/revisiongroupcollection/get_count/
---
## RevisionGroupCollection::get_Count method


Returnerar antalet revisionsgrupper i samlingen.

```cpp
int32_t Aspose::Words::RevisionGroupCollection::get_Count()
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

* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
