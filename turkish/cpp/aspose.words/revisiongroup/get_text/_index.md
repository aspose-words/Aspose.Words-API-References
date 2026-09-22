---
title: "Aspose::Words::RevisionGroup::get_Text metodu"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::RevisionGroup::get_Text metodu. C++ içinde eklenen/silinen/taşınan metni veya biçim değişikliği açıklamasını döndürür."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/revisiongroup/get_text/
---
## RevisionGroup::get_Text method


Eklenen/silinen/taşınan metni veya biçim değişikliği açıklamasını döndürür.

```cpp
System::String Aspose::Words::RevisionGroup::get_Text()
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
