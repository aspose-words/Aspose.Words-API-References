---
title: "Aspose::Words::RevisionGroup::get_Author method"
linktitle: "get_Author"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::RevisionGroup::get_Author method. Gibt den Autor dieser Revisionsgruppe in C++ zurück."
type: docs
weight: 2000
url: /de/cpp/aspose.words/revisiongroup/get_author/
---
## RevisionGroup::get_Author method


Liefert den Autor dieser Revisionsgruppe.

```cpp
System::String Aspose::Words::RevisionGroup::get_Author()
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

* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
