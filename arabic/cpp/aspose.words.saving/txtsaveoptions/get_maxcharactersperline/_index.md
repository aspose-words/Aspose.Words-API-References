---
title: "طريقة Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine"
linktitle: "get_MaxCharactersPerLine"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine. يحصل على أو يحدد قيمة عددية تحدد الحد الأقصى لعدد الأحرف في سطر واحد. القيمة الافتراضية هي 0، مما يعني عدم وجود حد في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/txtsaveoptions/get_maxcharactersperline/
---
## TxtSaveOptions::get_MaxCharactersPerLine method


يحصل أو يضبط قيمة عددية تحدد الحد الأقصى لعدد الأحرف في سطر واحد. القيمة الافتراضية هي 0، مما يعني عدم وجود حد.

```cpp
int32_t Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine() const
```


## أمثلة



يظهر كيفية تعيين الحد الأقصى لعدد الأحرف في كل سطر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// عيّن 30 حرفًا كحد أقصى مسموح به في سطر واحد.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_MaxCharactersPerLine(30);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

## انظر أيضًا

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
