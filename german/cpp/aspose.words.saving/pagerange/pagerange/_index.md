---
title: "Aspose::Words::Saving::PageRange::PageRange Konstruktor"
linktitle: "PageRange"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PageRange::PageRange Konstruktor. Erstellt ein neues Seitenbereichs‑Objekt in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.saving/pagerange/pagerange/
---
## PageRange::PageRange constructor


Erstellt ein neues PageRange-Objekt.

```cpp
Aspose::Words::Saving::PageRange::PageRange(int32_t from, int32_t to)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| von | int32_t | Der nullbasierte Index der Startseite. |
| bis | int32_t | Der nullbasierte Index der Endseite. Wenn er den Index der letzten Seite im Dokument überschreitet, wird er beim Rendern auf die Dokumentgröße gekürzt. |

## Beispiele



Zeigt, wie Seiten basierend auf genauen PageRanges extrahiert werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Siehe auch

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
