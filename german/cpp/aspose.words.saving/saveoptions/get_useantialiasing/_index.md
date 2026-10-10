---
title: "Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing Methode"
linktitle: "get_UseAntiAliasing"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob Antialiasing beim Rendern in C++ verwendet wird oder nicht."
type: docs
weight: 21000
url: /de/cpp/aspose.words.saving/saveoptions/get_useantialiasing/
---
## SaveOptions::get_UseAntiAliasing method


Ermittelt oder legt einen Wert fest, der bestimmt, ob Antialiasing beim Rendern verwendet werden soll.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing() const
```

## Hinweise


Der Standardwert ist **false**. Wenn dieser Wert auf **true** gesetzt wird, wird Antialiasing für das Rendern verwendet.

Diese Eigenschaft wird verwendet, wenn das Dokument in die folgenden Formate exportiert wird: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/). Wenn das Dokument in die Formate [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) oder [Mobi](../../../aspose.words/saveformat/) exportiert wird, wird diese Option für Rasterbilder verwendet.

## Beispiele



Zeigt, wie die Qualität eines gerenderten Dokuments mit [SaveOptions](../) verbessert werden kann.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```

## Siehe auch

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
