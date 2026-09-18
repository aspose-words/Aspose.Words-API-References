---
title: "Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes Methode"
linktitle: "get_RenderNonImageShapes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes Methode. Gibt einen Wert zurück oder legt ihn fest, der angibt, ob Nicht‑Bild‑Formen gerendert und in das ausgegebene Docling‑JSON‑Dokument geschrieben werden sollen in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/doclingsaveoptions/get_rendernonimageshapes/
---
## DoclingSaveOptions::get_RenderNonImageShapes method


Liest oder legt einen Wert fest, der angibt, ob Nicht-Bild-Formen gerendert und in das ausgegebene Docling-JSON-Dokument geschrieben werden sollen.

```cpp
bool Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes() const
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

* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
