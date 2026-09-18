---
title: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution Methode"
linktitle: "get_MaxImageResolution"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution Methode. Gibt einen Wert in Pixel pro Zoll zurück oder legt ihn fest, der die Auflösung exportierter Rasterbilder begrenzt. Der Standardwert ist Null in C++."
type: docs
weight: 4500
url: /de/cpp/aspose.words.saving/svgsaveoptions/get_maximageresolution/
---
## SvgSaveOptions::get_MaxImageResolution method


Liest oder legt einen Wert in Pixel pro Zoll fest, der die Auflösung exportierter Rasterbilder begrenzt. Der Standardwert ist null.

```cpp
int32_t Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution() const
```

## Hinweise


Wenn der Wert dieser Eigenschaft ungleich Null ist, begrenzt er die Auflösung exportierter Rasterbilder. Das bedeutet, Bilder mit höherer Auflösung werden auf das Limit heruntergerechnet und Bilder mit niedrigerer Auflösung werden unverändert exportiert.

Wenn der Wert dieser Eigenschaft Null ist, werden alle Rasterbilder ohne Resampling exportiert.

## Beispiele



Zeigt, wie man das Limit für die Bildauflösung festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Siehe auch

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
