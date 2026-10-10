---
title: "Metodo Aspose::Words::Rendering::NodeRendererBase::RenderToScale"
linktitle: "RenderToScale"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Rendering::NodeRendererBase::RenderToScale. Renderizza la forma in un oggetto Graphics a una scala specificata in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.rendering/noderendererbase/rendertoscale/
---
## NodeRendererBase::RenderToScale method


Renderizza la forma in un oggetto **Graphics** a una scala specificata.

```cpp
System::Drawing::SizeF Aspose::Words::Rendering::NodeRendererBase::RenderToScale(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | L'oggetto su cui renderizzare. |
| x | float | La coordinata X (in unità del mondo) dell'angolo superiore sinistro della forma renderizzata. |
| y | float | La coordinata Y (in unità del mondo) dell'angolo superiore sinistro della forma renderizzata. |
| scale | float | La scala per il rendering della forma (1.0 è 100%). |

### ReturnValue

La larghezza e l'altezza (in unità del mondo) della forma renderizzata.

## Vedi anche

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
