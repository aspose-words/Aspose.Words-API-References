---
title: "Aspose::Words::Saving::PageRange klass"
linktitle: "PageRange"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PageRange klass. Representerar ett kontinuerligt sidintervall. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.saving/pagerange/
---
## PageRange class


Representerar ett kontinuerligt sidintervall. För att lära dig mer, besök dokumentationsartikeln [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageRange : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageRange](./pagerange/)(int32_t, int32_t) | Skapar ett nytt sidintervallobjekt. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man extraherar sidor baserat på exakta sidintervall.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
