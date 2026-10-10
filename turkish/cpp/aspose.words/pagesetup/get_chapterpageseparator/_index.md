---
title: "Aspose::Words::PageSetup::get_ChapterPageSeparator yöntemi"
linktitle: "get_ChapterPageSeparator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_ChapterPageSeparator yöntemi. C++'ta bölüm numarası ile sayfa numarası arasında görünen ayırıcı karakteri alır veya ayarlar."
type: docs
weight: 11000
url: /tr/cpp/aspose.words/pagesetup/get_chapterpageseparator/
---
## PageSetup::get_ChapterPageSeparator method


Bölüm numarası ile sayfa numarası arasında görünen ayırıcı karakteri alır veya ayarlar.

```cpp
Aspose::Words::ChapterPageSeparator Aspose::Words::PageSetup::get_ChapterPageSeparator()
```

## Açıklamalar


Bölüm numaralarını içeren sayfa numaraları oluşturabilmek için, belge başlıklarının numaralı bir anahat biçimi uygulanmış olması gerekir.

## Örnekler



Sayfa bölümleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```

## Ayrıca Bakınız

* Enum [ChapterPageSeparator](../../chapterpageseparator/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
