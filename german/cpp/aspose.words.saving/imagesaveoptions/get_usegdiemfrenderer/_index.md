---
title: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer Methode"
linktitle: "get_UseGdiEmfRenderer"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer-Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob beim Speichern in EMF in C++ GDI+ oder der Aspose.Words-Metadatei-Renderer verwendet wird."
type: docs
weight: 18000
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_usegdiemfrenderer/
---
## ImageSaveOptions::get_UseGdiEmfRenderer method


Liest oder legt einen Wert fest, der bestimmt, ob beim Speichern nach EMF GDI+ oder der Aspose.Words‑Metadatei‑Renderer verwendet wird.

```cpp
bool Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer() const
```

## Hinweise


Wenn auf **true** gesetzt, wird der GDI+ Metadatei-Renderer verwendet. D.h. der Inhalt wird in ein GDI+ Grafikobjekt geschrieben und als Metadatei gespeichert.

Wenn auf **false** gesetzt, wird der Aspose.Words Metadatei-Renderer verwendet. D.h. der Inhalt wird direkt im Metadatei-Format mit Aspose.Words geschrieben.

Wirkt nur beim Speichern in EMF.

GDI+-Speichern funktioniert nur unter .NET.

Der Standardwert ist **true**.

## Beispiele



Zeigt, wie man einen Renderer auswählt, wenn ein Dokument in .emf konvertiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Wenn wir das Dokument als EMF-Bild speichern, können wir ein SaveOptions-Objekt übergeben, um einen Renderer für das Bild auszuwählen.
// Wenn wir das Flag "UseGdiEmfRenderer" auf "true" setzen, verwendet Aspose.Words den GDI+-Renderer.
// Wenn wir das Flag "UseGdiEmfRenderer" auf "false" setzen, verwendet Aspose.Words seinen eigenen Metadatei-Renderer.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Emf);
saveOptions->set_UseGdiEmfRenderer(useGdiEmfRenderer);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Renderer.emf", saveOptions);
```

## Siehe auch

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
