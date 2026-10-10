---
title: "Aspose::Words::Framesets::FramesetCollection sınıfı"
linktitle: "FramesetCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Framesets::FramesetCollection sınıfı. Frameset sınıfının örneklerinden oluşan bir koleksiyonu temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class


Frameset sınıfının örneklerinden oluşan bir koleksiyonu temsil eder. Daha fazla bilgi edinmek için [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) belge makalesini ziyaret edin.

```cpp
class FramesetCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Framesets::Frameset>>
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
| [FramesetCollection](./framesetcollection/)() |  |
| [get_Count](./get_count/)() | Koleksiyonda bulunan çerçeve veya çerçeve sayfalarının sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyon içinde yineleme yapan bir döngücü (enumerator) döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki bir çerçeve veya çerçeve sayfasını alır. |
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

## Örnekler



Sayfa üzerindeki çerçevelere nasıl erişileceğini gösterir.
```cpp
// Belge, diğer belgelere bağlantılar içeren birkaç çerçeve içerir.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Frameset.docx");

ASSERT_EQ(3, doc->get_Frameset()->get_ChildFramesets()->get_Count());
// Varsayılan URL'yi (bir web sayfası URL'si veya yerel belge) veya çerçevenin dış bir kaynak olup olmadığını kontrol edebiliriz.
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// Çerçevelerimizden birinin özelliklerini değiştirin.
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Framesets](../)
* Library [Aspose.Words for C++](../../)
