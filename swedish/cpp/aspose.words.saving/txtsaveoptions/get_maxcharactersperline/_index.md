---
title: "Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine metod"
linktitle: "get_MaxCharactersPerLine"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine metod. Hämtar eller anger ett heltalsvärde som specificerar det maximala antalet tecken per rad. Standardvärdet är 0, vilket betyder ingen gräns i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/txtsaveoptions/get_maxcharactersperline/
---
## TxtSaveOptions::get_MaxCharactersPerLine method


Hämtar eller anger ett heltalsvärde som specificerar det maximala antalet tecken per rad. Standardvärdet är 0, vilket betyder ingen gräns.

```cpp
int32_t Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine() const
```


## Exempel



Visar hur man ställer in maximalt antal tecken per rad.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Ställ in 30 tecken som maximalt tillåtet per rad.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_MaxCharactersPerLine(30);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

## Se även

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
