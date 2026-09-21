---
title: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution metod"
linktitle: "get_MaxImageResolution"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution metod. Hämtar eller anger ett värde i pixlar per tum som begränsar upplösningen för exporterade rasterbilder. Standardvärdet är noll i C++."
type: docs
weight: 4500
url: /sv/cpp/aspose.words.saving/svgsaveoptions/get_maximageresolution/
---
## SvgSaveOptions::get_MaxImageResolution method


Hämtar eller anger ett värde i pixlar per tum som begränsar upplösningen för exporterade rasterbilder. Standardvärdet är noll.

```cpp
int32_t Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution() const
```

## Anmärkningar


Om värdet för denna egenskap är icke-noll, begränsar det upplösningen för exporterade rasterbilder. Det vill säga, högupplösta bilder omprovsamplas ned till gränsen och lågupplösta bilder exporteras som de är.

Om värdet för denna egenskap är noll, exporteras alla rasterbilder utan omprovsampling.

## Exempel



Visar hur man anger en gräns för bildupplösning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Se även

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
