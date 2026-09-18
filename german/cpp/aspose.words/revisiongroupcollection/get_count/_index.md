---
title: "Aspose::Words::RevisionGroupCollection::get_Count Methode"
linktitle: "get_Count"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::RevisionGroupCollection::get_Count Methode. Gibt die Anzahl der Revisionsgruppen in der Sammlung in C++ zurück."
type: docs
weight: 6000
url: /de/cpp/aspose.words/revisiongroupcollection/get_count/
---
## RevisionGroupCollection::get_Count method


Gibt die Anzahl der Revisionsgruppen in der Sammlung zurück.

```cpp
int32_t Aspose::Words::RevisionGroupCollection::get_Count()
```


## Beispiele



Zeigt, wie man Informationen über eine Gruppe von Revisionen in einem Dokument ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```

## Siehe auch

* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
