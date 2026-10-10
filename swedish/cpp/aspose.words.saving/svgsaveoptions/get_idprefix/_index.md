---
title: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix metod"
linktitle: "get_IdPrefix"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix metod. Anger ett prefix som läggs före alla genererade element-ID:n i utdatafilen. Standardvärdet är null och inget prefix läggs till i C++."
type: docs
weight: 4250
url: /sv/cpp/aspose.words.saving/svgsaveoptions/get_idprefix/
---
## SvgSaveOptions::get_IdPrefix method


Anger ett prefix som läggs före alla genererade element-ID:n i utmatningsdokumentet. Standardvärdet är null och inget prefix läggs till.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix() const
```


## Exempel



Visar hur man lägger till ett prefix som läggs före alla genererade element-ID:n (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

## Se även

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
