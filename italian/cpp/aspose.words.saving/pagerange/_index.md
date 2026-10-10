---
title: "classe Aspose::Words::Saving::PageRange"
linktitle: "PageRange"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Saving::PageRange. Rappresenta un intervallo continuo di pagine. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.saving/pagerange/
---
## PageRange class


Rappresenta un intervallo continuo di pagine. Per saperne di più, visita l'articolo di documentazione [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageRange : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageRange](./pagerange/)(int32_t, int32_t) | Crea un nuovo oggetto intervallo di pagine. |
| static [Type](./type/)() |  |

## Esempi



Mostra come estrarre pagine basate su intervalli di pagine esatti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
