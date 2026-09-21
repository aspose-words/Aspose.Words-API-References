---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel metod"
linktitle: "get_CompressionLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel metod. Anger komprimeringsnivån som används för att spara dokumentet. Standardvärdet är Normal i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/ooxmlsaveoptions/get_compressionlevel/
---
## OoxmlSaveOptions::get_CompressionLevel method


Anger komprimeringsnivån som används för att spara dokumentet. Standardvärdet är [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel() const
```


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

## Se även

* Enum [CompressionLevel](../../compressionlevel/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
