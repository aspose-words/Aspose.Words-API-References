---
title: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode-Methode"
linktitle: "get_ImlRenderingMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode-Methode. Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie Tinten‑ (InkML‑)Objekte in C++ gerendert werden."
type: docs
weight: 10000
url: /de/cpp/aspose.words.saving/saveoptions/get_imlrenderingmode/
---
## SaveOptions::get_ImlRenderingMode method


Liest oder setzt einen Wert, der bestimmt, wie Tinten‑ (InkML‑)Objekte gerendert werden.

```cpp
Aspose::Words::Saving::ImlRenderingMode Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode() const
```

## Hinweise


Der Standardwert ist [InkML](../../imlrenderingmode/).

Diese Eigenschaft wird verwendet, wenn das Dokument in feste Seitenformate exportiert wird.

## Beispiele



Zeigt, wie ein Ink-Objekt gerendert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// Setzt 'ImlRenderingMode.InkML' ignoriert die Ersatzform des Tintenobjekts (InkML) und rendert das InkML selbst.
// Wenn das Rendering-Ergebnis unbefriedigend ist,
// verwenden Sie bitte 'ImlRenderingMode.Fallback', um ein Ergebnis zu erhalten, das früheren Versionen ähnelt.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## Siehe auch

* Enum [ImlRenderingMode](../../imlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
