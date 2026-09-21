---
title: "Aspose::Words::PageSetup::get_HeadingLevelForChapter metod"
linktitle: "get_HeadingLevelForChapter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_HeadingLevelForChapter metod. Hämtar eller anger stilnivån för rubriker som tillämpas på kapiteltitlarna i dokumentet i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words/pagesetup/get_headinglevelforchapter/
---
## PageSetup::get_HeadingLevelForChapter method


Hämtar eller anger rubriknivåstilen som tillämpas på kapiteltitlarna i dokumentet.

```cpp
int32_t Aspose::Words::PageSetup::get_HeadingLevelForChapter()
```

## Anmärkningar


Kan vara ett tal från 0 till 9. 0 betyder inget kapitelnumer om det tillämpas på sidnummer.

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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
