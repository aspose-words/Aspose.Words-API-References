---
title: "Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName metod"
linktitle: "get_FallbackFontName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName metod. Namnet på det teckensnitt som kommer att användas om inget förväntat teckensnitt hittas i skrivaren och i de inbyggda teckensnittssamlingarna i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/pclsaveoptions/get_fallbackfontname/
---
## PclSaveOptions::get_FallbackFontName method


Namnet på teckensnittet som kommer att användas om inget förväntat teckensnitt hittas i skrivaren och de inbyggda teckensnittssamlingarna.

```cpp
System::String Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName() const
```


## Exempel



Visar hur man deklarerar ett teckensnitt som en skrivare kommer att använda för tryckt text som ersättning om det ursprungliga teckensnittet inte är tillgängligt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_FallbackFontName(u"Times New Roman");

// Detta dokument kommer att instruera skrivaren att använda "Times New Roman" för texten med det saknade teckensnittet.
// Om "Times New Roman" också är otillgängligt, kommer skrivaren att använda standardfonten "Arial".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

## Se även

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
