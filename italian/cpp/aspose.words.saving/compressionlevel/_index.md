---
title: "Aspose::Words::Saving::CompressionLevel enum"
linktitle: "CompressionLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::CompressionLevel enum. Livello di compressione per file OOXML e XPS. (I file DOCX, DOTX e XPS sono internamente un archivio ZIP, questa proprietà controlla il livello di compressione dell'archivio. Nota che il file FlatOpc non è un archivio ZIP, quindi questa proprietà non influisce sui file FlatOpc.) in C++."
type: docs
weight: 47000
url: /it/cpp/aspose.words.saving/compressionlevel/
---
## CompressionLevel enum


Livello di compressione per i file OOXML e XPS. (I file DOCX, DOTX e XPS sono internamente un archivio ZIP; questa proprietà controlla il livello di compressione dell'archivio. Nota che il file FlatOpc non è un archivio ZIP, quindi questa proprietà non influisce sui file FlatOpc.)

```cpp
enum class CompressionLevel
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Normal | 0 | Livello di compressione normale. Livello di compressione predefinito utilizzato da [Aspose.Words](../../aspose.words/). |
| Maximum | 1 | Livello di compressione massimo. |
| Fast | 2 | Livello di compressione veloce. |
| SuperFast | 3 | Livello di compressione super veloce. Microsoft Word utilizza questo livello di compressione. |


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


Mostra come controllare il livello di compressione durante il salvataggio di un documento in formato XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Crea un oggetto XpsSaveOptions e imposta il livello di compressione.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
