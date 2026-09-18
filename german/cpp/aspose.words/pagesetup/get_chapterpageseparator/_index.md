---
title: "Aspose::Words::PageSetup::get_ChapterPageSeparator Methode"
linktitle: "get_ChapterPageSeparator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_ChapterPageSeparator Methode. Gibt an oder legt das Trennzeichen fest, das zwischen der Kapitelnummer und der Seitenzahl erscheint, in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words/pagesetup/get_chapterpageseparator/
---
## PageSetup::get_ChapterPageSeparator method


Liest oder legt das Trennzeichen fest, das zwischen der Kapitelnummer und der Seitenzahl erscheint.

```cpp
Aspose::Words::ChapterPageSeparator Aspose::Words::PageSetup::get_ChapterPageSeparator()
```

## Hinweise


Bevor Sie Seitenzahlen erstellen können, die Kapitelnummern enthalten, müssen die Dokumentüberschriften ein nummeriertes Gliederungsformat erhalten.

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

* Enum [ChapterPageSeparator](../../chapterpageseparator/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
