---
title: "Aspose::Words::RevisionGroup class"
linktitle: "RevisionGroup"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::RevisionGroup sınıfı. Ardışık Revision nesnelerinden oluşan bir grup temsil eder. Daha fazla bilgi için C++'deki belge makalesini ziyaret edin."
type: docs
weight: 54000
url: /tr/cpp/aspose.words/revisiongroup/
---
## RevisionGroup class


Ardışık [Revision](../revision/) nesnelerinden oluşan bir grup temsil eder. Daha fazla bilgi için [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/) belge makalesini ziyaret edin.

```cpp
class RevisionGroup : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Author](./get_author/)() | Bu revizyon grubunun yazarını alır. |
| [get_RevisionType](./get_revisiontype/)() | Bu grupta bulunan revizyonların türünü alır. |
| [get_Text](./get_text/)() | Eklenen/silinen/taşınan metni veya biçim değişikliği açıklamasını döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
