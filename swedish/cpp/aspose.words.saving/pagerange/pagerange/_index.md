---
title: "Aspose::Words::Saving::PageRange::PageRange konstruktor"
linktitle: "PageRange"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PageRange::PageRange konstruktor. Skapar ett nytt sidintervallobjekt i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.saving/pagerange/pagerange/
---
## PageRange::PageRange constructor


Skapar ett nytt sidintervallobjekt.

```cpp
Aspose::Words::Saving::PageRange::PageRange(int32_t from, int32_t to)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| från | int32_t | Den startande sidans nollbaserade index. |
| till | int32_t | Den avslutande sidans nollbaserade index. Om den överstiger index för den sista sidan i dokumentet trunkeras den för att passa in i dokumentet vid rendering. |

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

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
