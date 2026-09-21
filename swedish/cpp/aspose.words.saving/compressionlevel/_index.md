---
title: "Aspose::Words::Saving::CompressionLevel enum"
linktitle: "CompressionLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::CompressionLevel enum. Komprimeringsnivå för OOXML- och XPS-filer. (DOCX-, DOTX- och XPS-filer är internt ett ZIP‑arkiv, den här egenskapen styr komprimeringsnivån för arkivet. Observera att FlatOpc‑filen inte är ett ZIP‑arkiv, därför påverkar inte den här egenskapen FlatOpc‑filerna.) i C++."
type: docs
weight: 47000
url: /sv/cpp/aspose.words.saving/compressionlevel/
---
## CompressionLevel enum


Komprimeringsnivå för OOXML- och XPS-filer. (DOCX-, DOTX- och XPS-filer är internt ett ZIP-arkiv, den här egenskapen styr komprimeringsnivån för arkivet. Observera att FlatOpc-filen inte är ett ZIP-arkiv, därför påverkar inte den här egenskapen FlatOpc-filerna.)

```cpp
enum class CompressionLevel
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Normal | 0 | Normal komprimeringsnivå. Standardkomprimeringsnivå som används av [Aspose.Words](../../aspose.words/). |
| Maximum | 1 | Maximal komprimeringsnivå. |
| Snabb | 2 | Snabb komprimeringsnivå. |
| SuperSnabb | 3 | Super Snabb komprimeringsnivå. Microsoft Word använder denna komprimeringsnivå. |


## Exempel



Visar hur man anger den komprimeringsnivå som ska användas vid sparande av ett OOXML-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// När vi sparar dokumentet i ett OOXML-format kan vi skapa ett OoxmlSaveOptions‑objekt.
// och sedan skicka den till dokumentets sparningsmetod för att ändra hur vi sparar dokumentet.
// Ställ in egenskapen "CompressionLevel" till "CompressionLevel.Maximum" för att tillämpa den starkaste och långsammaste komprimeringen.
// Ställ in egenskapen "CompressionLevel" till "CompressionLevel.Normal" för att tillämpa
// standardkomprimeringen som Aspose.Words använder när OOXML-dokument sparas.
// Ställ in egenskapen "CompressionLevel" till "CompressionLevel.Fast" för att tillämpa en snabbare och svagare komprimering.
// Ställ in egenskapen "CompressionLevel" till "CompressionLevel.SuperFast" för att tillämpa
// standardkomprimeringen som Microsoft Word använder.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_CompressionLevel(compressionLevel);

System::SharedPtr<System::Diagnostics::Stopwatch> st = System::Diagnostics::Stopwatch::StartNew();
doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st->Stop();

auto fileInfo = System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"OoxmlSaveOptions.DocumentCompression.docx");

std::cout << System::String::Format(u"Saving operation done using the \"{0}\" compression level:", compressionLevel) << std::endl;
std::cout << System::String::Format(u"\tDuration:\t{0} ms", st->get_ElapsedMilliseconds()) << std::endl;
std::cout << System::String::Format(u"\tFile Size:\t{0} bytes", fileInfo->get_Length()) << std::endl;
```


Visar hur man styr komprimeringsnivån när ett dokument sparas i XPS-format.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Skapa ett XpsSaveOptions-objekt och ange komprimeringsnivån.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
