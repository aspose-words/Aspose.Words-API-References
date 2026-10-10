---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel Methode"
linktitle: "get_CompressionLevel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel Methode. Gibt das Kompressionslevel an, das zum Speichern des Dokuments verwendet wird. Der Standardwert ist Normal in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/ooxmlsaveoptions/get_compressionlevel/
---
## OoxmlSaveOptions::get_CompressionLevel method


Gibt das Kompressionslevel an, das zum Speichern des Dokuments verwendet wird. Der Standardwert ist [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel() const
```


## Beispiele



Zeigt, wie die beim Speichern eines OOXML-Dokuments zu verwendende Komprimierungsstufe angegeben wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Wenn wir das Dokument in ein OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
// und es dann an die Speichermethode des Dokuments übergeben, um zu ändern, wie wir das Dokument speichern.
// Setzen Sie die Eigenschaft "CompressionLevel" auf "CompressionLevel.Maximum", um die stärkste und langsamste Kompression anzuwenden.
// Setzen Sie die Eigenschaft "CompressionLevel" auf "CompressionLevel.Normal", um anzuwenden
// die Standardkompression, die Aspose.Words beim Speichern von OOXML-Dokumenten verwendet.
// Setzen Sie die Eigenschaft "CompressionLevel" auf "CompressionLevel.Fast", um eine schnellere und schwächere Kompression anzuwenden.
// Setzen Sie die Eigenschaft "CompressionLevel" auf "CompressionLevel.SuperFast", um anzuwenden
// die Standardkompression, die Microsoft Word verwendet.
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

## Siehe auch

* Enum [CompressionLevel](../../compressionlevel/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
