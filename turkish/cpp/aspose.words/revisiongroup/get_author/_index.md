---
title: "Aspose::Words::RevisionGroup::get_Author metodu"
linktitle: "get_Author"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::RevisionGroup::get_Author metodu. Bu revizyon grubunun yazarını C++ içinde alır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/revisiongroup/get_author/
---
## RevisionGroup::get_Author method


Bu revizyon grubunun yazarını alır.

```cpp
System::String Aspose::Words::RevisionGroup::get_Author()
```


## Örnekler



Bir belgede revizyon grubuyla ilgili bilgilerin nasıl yazdırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```

## Ayrıca Bakınız

* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
