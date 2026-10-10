---
title: "Aspose::Words::Rendering::NodeRendererBase::RenderToScale Methode"
linktitle: "RenderToScale"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Rendering::NodeRendererBase::RenderToScale Methode. Rendert die Form in ein Graphics‑Objekt mit einem angegebenen Maßstab in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.rendering/noderendererbase/rendertoscale/
---
## NodeRendererBase::RenderToScale method


Rendert die Form in ein **Graphics**-Objekt zu einem angegebenen Maßstab.

```cpp
System::Drawing::SizeF Aspose::Words::Rendering::NodeRendererBase::RenderToScale(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Das Objekt, in das gerendert werden soll. |
| x | float | Die X‑Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Form. |
| y | float | Die Y‑Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Form. |
| scale | float | Der Maßstab für das Rendern der Form (1,0 entspricht 100 %). |

### ReturnValue

Die Breite und Höhe (in Welteinheiten) der gerenderten Form.

## Siehe auch

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
