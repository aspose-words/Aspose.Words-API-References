---
title: "Aspose::Words::Saving::PclSaveOptions::AddPrinterFont‑metod"
linktitle: "AddPrinterFont"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PclSaveOptions::AddPrinterFont‑metod. Lägger till information om teckensnitt som laddas upp till skrivaren av tillverkaren i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions::AddPrinterFont method


Lägger till information om teckensnitt som laddas upp till skrivaren av tillverkaren.

```cpp
void Aspose::Words::Saving::PclSaveOptions::AddPrinterFont(const System::String &fontFullName, const System::String &fontPclName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontFullName | const System::String\& | Fullständigt namn på teckensnittet (t.ex. "Times New Roman Bold Italic"). |
| fontPclName | const System::String\& | Namnet på teckensnittet som används i Pcl-dokumentet. |

## Exempel



Visar hur man får en skrivare att ersätta alla förekomster av ett specifikt teckensnitt med ett annat teckensnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Courier");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->AddPrinterFont(u"Courier New", u"Courier");

// När detta dokument skrivs ut kommer skrivaren att använda teckensnittet "Courier New"
// för att komma åt ställen där vårt dokument använde teckensnittet "Courier".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

## Se även

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
