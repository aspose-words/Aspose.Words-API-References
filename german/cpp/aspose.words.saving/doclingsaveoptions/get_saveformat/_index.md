---
title: "Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat-Methode"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat-Methode. Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses SaveOptions-Objekt verwendet wird. Kann in C++ nur Docling sein."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/doclingsaveoptions/get_saveformat/
---
## DoclingSaveOptions::get_SaveFormat method


Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses SaveOptions-Objekt verwendet wird. Kann nur [Docling](../../../aspose.words/saveformat/) sein.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat() override
```


## Beispiele



Zeigt, wie ein Dokument im Docling-JSON-Format gespeichert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// Auf true setzen, um Nicht-Bild-Formen zu rendern und in die Ausgabe einzuschließen.
// Auf false (Standard) setzen, um Nicht-Bild-Formen von der Ausgabe auszuschließen.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
