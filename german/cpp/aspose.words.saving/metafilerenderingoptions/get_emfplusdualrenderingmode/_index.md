---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode Methode"
linktitle: "get_EmfPlusDualRenderingMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, wie EMF+ Dual-Metadateien in C++ gerendert werden sollen."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::get_EmfPlusDualRenderingMode method


Liest oder legt einen Wert fest, der bestimmt, wie EMF+ Dual-Metadateien gerendert werden sollen.

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```

## Hinweise


EMF+ Dual-Metadateien enthalten sowohl EMF+ als auch EMF‑Teile. MS Word und GDI+ rendern immer den EMF+-Teil. Aspose.Words unterstützt derzeit nicht alle EMF+-Datensätze vollständig, und in einigen Fällen sieht das Rendering‑Ergebnis des EMF‑Teils besser aus als das des EMF+-Teils.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird. Wird die Metadatei in ein Bitmap gerendert, wird immer der EMF+-Teil verwendet.

Der Standardwert ist [EmfPlusWithFallback](../../emfplusdualrenderingmode/).
## Siehe auch

* Enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
