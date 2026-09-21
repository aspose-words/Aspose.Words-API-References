---
title: "Aspose::Words::ChapterPageSeparator enum"
linktitle: "ChapterPageSeparator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ChapterPageSeparator enum. Definierar separatortecknet som visas mellan kapitlet och sidnumret i C++."
type: docs
weight: 84000
url: /sv/cpp/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enum


Definierar separator-tecknet som visas mellan kapitel- och sidnummer.

```cpp
enum class ChapterPageSeparator
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Bindestreck | 0 | Ett kolon. |
| Punkt | 1 | En punkt. |
| Kolon | 2 | Ett kolon. |
| Em‑streck | 3 | Ett betonat streck. |
| En‑streck | 4 | Ett standardstreck. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
