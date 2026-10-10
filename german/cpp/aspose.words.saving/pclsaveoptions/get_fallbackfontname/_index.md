---
title: "Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName Methode"
linktitle: "get_FallbackFontName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName Methode. Name der Schriftart, die verwendet wird, wenn keine erwartete Schriftart in den Drucker‑ und integrierten Schriftarten‑Sammlungen in C++ gefunden wird."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/pclsaveoptions/get_fallbackfontname/
---
## PclSaveOptions::get_FallbackFontName method


Name der Schriftart, die verwendet wird, wenn keine erwartete Schriftart im Drucker und in den integrierten Schriftartsammlungen gefunden wird.

```cpp
System::String Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName() const
```


## Beispiele



Zeigt, wie man eine Schriftart deklariert, die ein Drucker als Ersatz auf den gedruckten Text anwendet, falls die Originalschriftart nicht verfügbar ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_FallbackFontName(u"Times New Roman");

// Dieses Dokument weist den Drucker an, "Times New Roman" auf den Text mit der fehlenden Schriftart anzuwenden.
// Sollte \"Times New Roman\" ebenfalls nicht verfügbar sein, verwendet der Drucker standardmäßig die Schriftart \"Arial\".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

## Siehe auch

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
