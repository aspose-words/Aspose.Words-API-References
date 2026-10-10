---
title: "metodo Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel"
linktitle: "get_CompressionLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel method. Specifica il livello di compressione utilizzato per salvare il documento. Il valore predefinito è Normal in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/ooxmlsaveoptions/get_compressionlevel/
---
## OoxmlSaveOptions::get_CompressionLevel method


Specifica il livello di compressione usato per salvare il documento. Il valore predefinito è [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel() const
```


## Esempi



Mostra come specificare il livello di compressione da utilizzare durante il salvataggio di un documento OOXML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Quando salviamo il documento in un formato OOXML, possiamo creare un oggetto OoxmlSaveOptions
// e poi passarlo al metodo di salvataggio del documento per modificare il modo in cui salviamo il documento.
// Imposta la proprietà "CompressionLevel" su "CompressionLevel.Maximum" per applicare la compressione più forte e più lenta.
// Imposta la proprietà "CompressionLevel" su "CompressionLevel.Normal" per applicare
// la compressione predefinita che Aspose.Words utilizza durante il salvataggio dei documenti OOXML.
// Imposta la proprietà "CompressionLevel" su "CompressionLevel.Fast" per applicare una compressione più veloce e più debole.
// Imposta la proprietà "CompressionLevel" su "CompressionLevel.SuperFast" per applicare
// la compressione predefinita che Microsoft Word utilizza.
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

## Vedi anche

* Enum [CompressionLevel](../../compressionlevel/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
