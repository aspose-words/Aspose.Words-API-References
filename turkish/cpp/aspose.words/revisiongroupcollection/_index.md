---
title: "Aspose::Words::RevisionGroupCollection sınıfı"
linktitle: "RevisionGroupCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::RevisionGroupCollection sınıfı. Belgede revizyon gruplarını temsil eden RevisionGroup nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 55000
url: /tr/cpp/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class


Belgede revizyon gruplarını temsil eden [RevisionGroup](../revisiongroup/) nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/) belge makalesini ziyaret edin.

```cpp
class RevisionGroupCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::RevisionGroup>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyondaki revizyon grubu sayısını döndürür. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki bir revizyon grubunu döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Açıklama |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Açıklamalar


Bu sınıfın örneklerini doğrudan oluşturmazsınız. Bir belgede bulunan revizyon gruplarını almak için [Groups](../revisioncollection/get_groups/) özelliğini kullanın.

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


Bir belgede revizyon grubunun nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
