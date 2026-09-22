---
title: "Aspose::Words::Framesets::FramesetCollection::get_Count metodu"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Framesets::FramesetCollection::get_Count metodu. C++'de koleksiyonda bulunan çerçevelerin veya çerçeve sayfalarının sayısını alır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.framesets/framesetcollection/get_count/
---
## FramesetCollection::get_Count method


Koleksiyonda bulunan çerçeve veya çerçeve sayfalarının sayısını alır.

```cpp
int32_t Aspose::Words::Framesets::FramesetCollection::get_Count()
```


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

* Class [FramesetCollection](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
