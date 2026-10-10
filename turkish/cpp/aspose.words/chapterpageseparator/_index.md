---
title: "Aspose::Words::ChapterPageSeparator enum"
linktitle: "ChapterPageSeparator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ChapterPageSeparator enum. C++'da bölüm ve sayfa numarası arasında görülen ayırıcı karakteri tanımlar."
type: docs
weight: 84000
url: /tr/cpp/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enum


Bölüm ve sayfa numarası arasında görünen ayırıcı karakteri tanımlar.

```cpp
enum class ChapterPageSeparator
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Tire | 0 | Bir iki nokta üst üste. |
| Nokta | 1 | Bir nokta. |
| İki nokta üst üste | 2 | Bir iki nokta üst üste. |
| EmDash | 3 | Vurgulanan bir tire. |
| EnDash | 4 | Standart bir tire. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
