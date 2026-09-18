---
title: "Aspose::Words::PageSetup::get_HeadingLevelForChapter Methode"
linktitle: "get_HeadingLevelForChapter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_HeadingLevelForChapter Methode. Liest oder setzt den Überschriftenebenen‑Stil, der auf die Kapitelüberschriften im Dokument angewendet wird, in C++."
type: docs
weight: 20000
url: /de/cpp/aspose.words/pagesetup/get_headinglevelforchapter/
---
## PageSetup::get_HeadingLevelForChapter method


Liest oder legt den Überschriftenebenenstil fest, der auf die Kapiteltitel im Dokument angewendet wird.

```cpp
int32_t Aspose::Words::PageSetup::get_HeadingLevelForChapter()
```

## Hinweise


Kann eine Zahl von 0 bis 9 sein. 0 bedeutet keine Kapitelnummer, wenn sie auf die Seitenzahl angewendet wird.

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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
