---
title: "Aspose::Words::Lists::ListCollection::GetListByListId method"
linktitle: "GetListByListId"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListCollection::GetListByListId yöntemi. C++'da bir liste tanımlayıcısı ile liste alır."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection::GetListByListId method


Bir liste tanımlayıcısı ile bir liste alır.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::GetListByListId(int32_t listId)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| listId | int32_t | Liste tanımlayıcısı. |

### ReturnValue

Liste nesnesini döndürür. Belirtilen tanımlayıcıya sahip bir liste bulunamazsa **null** döndürür.
## Açıklamalar


Bu yöntemi normalde kullanmanız gerekmez. Çoğu zaman, paragraflara liste biçimlendirmesini sadece [List](../../listformat/get_list/) özelliğini [ListFormat](../../listformat/) nesnesinin ayarlayarak uygularsınız.

## Örnekler



Listelerin sahip belge özelliklerini nasıl doğrulayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::ListCollection> lists = doc->get_Lists();
ASPOSE_ASSERT_EQ(doc, lists->get_Document());

System::SharedPtr<Aspose::Words::Lists::List> list = lists->Add(Aspose::Words::Lists::ListTemplate::BulletDefault);
ASPOSE_ASSERT_EQ(doc, list->get_Document());

std::cout << (System::String(u"Current list count: ") + lists->get_Count()) << std::endl;
std::cout << (System::String(u"Is the first document list: ") + (System::ObjectExt::Equals(lists->idx_get(0), list))) << std::endl;
std::cout << (System::String(u"ListId: ") + list->get_ListId()) << std::endl;
std::cout << (System::String(u"List is the same by ListId: ") + (System::ObjectExt::Equals(lists->GetListByListId(1), list))) << std::endl;
```

## Ayrıca Bakınız

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
