---
title: "Aspose::Words::Saving::PageSavingArgs Klasse"
linktitle: "PageSavingArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PageSavingArgs Klasse. Stellt Daten für das PageSaving()-Ereignis bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 19000
url: /de/cpp/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class


Stellt Daten für das [PageSaving()](../ipagesavingcallback/pagesaving/) Ereignis bereit. Weitere Informationen finden Sie im [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) Dokumentationsartikel.

```cpp
class PageSavingArgs : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_KeepPageStreamOpen](./get_keeppagestreamopen/)() const | Gibt an, ob Aspose.Words den Stream nach dem Speichern einer Dokumentenseite offen halten oder schließen soll. |
| [get_PageFileName](./get_pagefilename/)() const | Ermittelt den Dateinamen, in dem die Dokumentenseite gespeichert wird. |
| [get_PageIndex](./get_pageindex/)() const | Aktueller Seitenindex. |
| [get_PageStream](./get_pagestream/)() const | Ermöglicht die Angabe des Streams, in dem die Dokumentenseite gespeichert wird. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSavingArgs](./pagesavingargs/)() |  |
| [set_KeepPageStreamOpen](./set_keeppagestreamopen/)(bool) | Setter für [Aspose::Words::Saving::PageSavingArgs::get_KeepPageStreamOpen](./get_keeppagestreamopen/). |
| [set_PageFileName](./set_pagefilename/)(const System::String\&) | Legt den Dateinamen fest, in dem die Dokumentenseite gespeichert wird. |
| [set_PageStream](./set_pagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter für [Aspose::Words::Saving::PageSavingArgs::get_PageStream](./get_pagestream/). |
| [set_PageStream](./set_pagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
