---
title: "Aspose::Words::Saving::ImlRenderingMode enum"
linktitle: "ImlRenderingMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImlRenderingMode enum. Gibt an, wie Tintenobjekte (InkML) in feste Seitenformate in C++ gerendert werden."
type: docs
weight: 66000
url: /de/cpp/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enum


Gibt an, wie Tinten‑ (InkML‑)Objekte in feste Seitenformate gerendert werden.

```cpp
enum class ImlRenderingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Fallback | 0 | Wenn für das Tintenobjekt (InkML) eine Ersatzform verfügbar ist, rendert Aspose.Words die Ersatzform anstelle des InkML. |
| InkML | 1 | Aspose.Words ignoriert die Ersatzform des Tintenobjekts (InkML) und rendert das InkML selbst. Dies ist der Standardmodus. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
