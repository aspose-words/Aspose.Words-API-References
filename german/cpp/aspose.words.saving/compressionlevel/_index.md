---
title: "Aspose::Words::Saving::CompressionLevel Enum"
linktitle: "CompressionLevel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::CompressionLevel Enum. Komprimierungsstufe für OOXML- und XPS-Dateien. (DOCX-, DOTX- und XPS-Dateien sind intern ein ZIP-Archiv, diese Eigenschaft steuert die Komprimierungsstufe des Archivs. Hinweis: Die FlatOpc-Datei ist kein ZIP-Archiv, daher wirkt sich diese Eigenschaft nicht auf FlatOpc-Dateien aus.) in C++."
type: docs
weight: 47000
url: /de/cpp/aspose.words.saving/compressionlevel/
---
## CompressionLevel enum


Komprimierungsgrad für OOXML- und XPS-Dateien. (DOCX-, DOTX- und XPS-Dateien sind intern ein ZIP-Archiv; diese Eigenschaft steuert den Komprimierungsgrad des Archivs. Hinweis: FlatOpc-Dateien sind kein ZIP-Archiv, daher wirkt sich diese Eigenschaft nicht auf FlatOpc-Dateien aus.)

```cpp
enum class CompressionLevel
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Normal | 0 | Normale Komprimierungsstufe. Standardkomprimierungsstufe, die von [Aspose.Words](../../aspose.words/) verwendet wird. |
| Maximum | 1 | Maximale Komprimierungsstufe. |
| Schnell | 2 | Schnelle Komprimierungsstufe. |
| SuperFast | 3 | Super schnelle Komprimierungsstufe. Microsoft Word verwendet diese Komprimierungsstufe. |


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


Zeigt, wie man die Komprimierungsstufe beim Speichern eines Dokuments im XPS-Format steuert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Erstellen Sie ein XpsSaveOptions-Objekt und setzen Sie die Komprimierungsstufe.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
