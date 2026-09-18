---
title: "Aspose::Words::Saving::PclSaveOptions::AddPrinterFont-Methode"
linktitle: "AddPrinterFont"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PclSaveOptions::AddPrinterFont-Methode. Fügt Informationen über die Schriftart hinzu, die vom Hersteller zum Drucker hochgeladen wird, in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions::AddPrinterFont method


Fügt Informationen über die Schriftart hinzu, die vom Hersteller zum Drucker hochgeladen wird.

```cpp
void Aspose::Words::Saving::PclSaveOptions::AddPrinterFont(const System::String &fontFullName, const System::String &fontPclName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFullName | const System::String\& | Vollständiger Name der Schriftart (z. B. "Times New Roman Bold Italic"). |
| fontPclName | const System::String\& | Name der Schriftart, die im Pcl-Dokument verwendet wird. |

## Beispiele



Zeigt, wie ein Drucker alle Vorkommen einer bestimmten Schriftart durch eine andere Schriftart ersetzen kann.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Courier");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->AddPrinterFont(u"Courier New", u"Courier");

// Beim Drucken dieses Dokuments verwendet der Drucker die Schriftart "Courier New"
// um Stellen zu erreichen, an denen unser Dokument die Schriftart "Courier" verwendet hat.
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

## Siehe auch

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
