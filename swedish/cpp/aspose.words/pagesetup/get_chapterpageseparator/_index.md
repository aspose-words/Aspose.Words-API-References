---
title: "Aspose::Words::PageSetup::get_ChapterPageSeparator‑metod"
linktitle: "get_ChapterPageSeparator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_ChapterPageSeparator‑metod. Hämtar eller anger separator‑tecknet som visas mellan kapitelnummret och sidnumret i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words/pagesetup/get_chapterpageseparator/
---
## PageSetup::get_ChapterPageSeparator method


Hämtar eller anger separator‑tecknet som visas mellan kapitelnummret och sidnumret.

```cpp
Aspose::Words::ChapterPageSeparator Aspose::Words::PageSetup::get_ChapterPageSeparator()
```

## Anmärkningar


Innan du kan skapa sidnummer som inkluderar kapitelnummret, måste dokumentrubrikerna ha ett numrerat dispositionsformat tillämpat.

## Exempel



Visar hur man arbetar med sidkapitel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```

## Se även

* Enum [ChapterPageSeparator](../../chapterpageseparator/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
