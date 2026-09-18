---
title: "Aspose::Words::Saving::PageRange Klasse"
linktitle: "PageRange"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PageRange Klasse. Stellt einen zusammenhängenden Seitenbereich dar. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 18000
url: /de/cpp/aspose.words.saving/pagerange/
---
## PageRange class


Stellt einen zusammenhängenden Seitenbereich dar. Weitere Informationen finden Sie im Dokumentationsartikel [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageRange : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageRange](./pagerange/)(int32_t, int32_t) | Erstellt ein neues PageRange-Objekt. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
