---
title: "Aspose::Words::RevisionGroupCollection::get_Count yöntemi"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::RevisionGroupCollection::get_Count yöntemi. C++'ta koleksiyondaki revizyon gruplarının sayısını döndürür."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/revisiongroupcollection/get_count/
---
## RevisionGroupCollection::get_Count method


Koleksiyondaki revizyon grubu sayısını döndürür.

```cpp
int32_t Aspose::Words::RevisionGroupCollection::get_Count()
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

* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
