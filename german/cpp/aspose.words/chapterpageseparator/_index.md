---
title: "Aspose::Words::ChapterPageSeparator enum"
linktitle: "ChapterPageSeparator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ChapterPageSeparator enum. Definiert das Trennzeichenzeichen, das in C++ zwischen Kapitel- und Seitennummer erscheint."
type: docs
weight: 84000
url: /de/cpp/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enum


Definiert das Trennzeichenzeichen, das zwischen Kapitel- und Seitennummer erscheint.

```cpp
enum class ChapterPageSeparator
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Bindestrich | 0 | Ein Doppelpunkt. |
| Punkt | 1 | Ein Punkt. |
| Doppelpunkt | 2 | Ein Doppelpunkt. |
| Gedankenstrich | 3 | Ein betonter Strich. |
| Halbgeviertstrich | 4 | Ein Standardstrich. |


## Beispiele



Zeigt, wie man mit Seitenkapiteln arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
