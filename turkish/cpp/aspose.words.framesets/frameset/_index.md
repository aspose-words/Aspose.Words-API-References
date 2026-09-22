---
title: "Aspose::Words::Framesets::Frameset class"
linktitle: "Frameset"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Framesets::Frameset class. Çerçeveler sayfasını veya bir çerçeve sayfasındaki tek bir çerçeveyi temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.framesets/frameset/
---
## Frameset class


Bir çerçeve sayfasını veya bir çerçeve sayfasındaki tek bir çerçeveyi temsil eder. Daha fazla bilgi edinmek için [Belgelerle Programlama](https://docs.aspose.com/words/cpp/programming-with-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
class Frameset : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Frameset](./frameset/)() |  |
| [get_ChildFramesets](./get_childframesets/)() const | Alt çerçevelerin ve çerçeve sayfalarının koleksiyonunu alır. |
| [get_FrameDefaultUrl](./get_framedefaulturl/)() | Bu çerçevede görüntülenecek web sayfası URL'sini veya belge dosya adını alır veya ayarlar. |
| [get_IsFrameLinkToFile](./get_isframelinktofile/)() | Çerçevenin bağlandığı harici bir kaynak olup olmadığını gösteren değeri, [FrameDefaultUrl](./get_framedefaulturl/) özelliğinde belirtilen web sayfası veya belge dosya adı için alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FrameDefaultUrl](./set_framedefaulturl/)(const System::String\&) | [Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl](./get_framedefaulturl/) için ayarlayıcı. |
| [set_IsFrameLinkToFile](./set_isframelinktofile/)(bool) | [Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile](./get_isframelinktofile/) için ayarlayıcı. |
| static [Type](./type/)() |  |

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
