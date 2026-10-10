---
title: "Aspose::Words::PageSetup::get_HeadingLevelForChapter metodu"
linktitle: "get_HeadingLevelForChapter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_HeadingLevelForChapter metodu. C++'ta belgede bölüm başlıklarına uygulanan başlık seviyesi stilini alır veya ayarlar."
type: docs
weight: 20000
url: /tr/cpp/aspose.words/pagesetup/get_headinglevelforchapter/
---
## PageSetup::get_HeadingLevelForChapter method


Belgedeki bölüm başlıklarına uygulanan başlık seviyesi stilini alır veya ayarlar.

```cpp
int32_t Aspose::Words::PageSetup::get_HeadingLevelForChapter()
```

## Açıklamalar


0 ile 9 arasında bir sayı olabilir. 0, sayfa numarasına uygulandığında bölüm numarası olmadığını ifade eder.

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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
