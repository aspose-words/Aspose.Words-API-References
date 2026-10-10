---
title: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize-Methode"
linktitle: "RenderToSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize-Methode. Rendert die Form in ein Graphics-Objekt auf eine angegebene Größe in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase::RenderToSize method


Rendert die Form in ein **Graphics**-Objekt mit einer angegebenen Größe.

```cpp
float Aspose::Words::Rendering::NodeRendererBase::RenderToSize(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Das Objekt, in das gerendert werden soll. |
| x | float | Die X‑Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Form. |
| y | float | Die Y‑Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Form. |
| Breite | float | Die maximale Breite (in Welteinheiten), die die gerenderte Form einnehmen kann. |
| Höhe | float | Die maximale Höhe (in Welteinheiten), die die gerenderte Form einnehmen kann. |

### ReturnValue

Der Maßstab, der automatisch für die gerenderte Form berechnet wurde, um die angegebene Größe zu passen.

## Siehe auch

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
