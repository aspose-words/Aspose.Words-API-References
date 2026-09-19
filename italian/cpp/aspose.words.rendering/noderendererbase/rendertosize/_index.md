---
title: "Metodo Aspose::Words::Rendering::NodeRendererBase::RenderToSize"
linktitle: "RenderToSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Rendering::NodeRendererBase::RenderToSize. Renderizza la forma in un oggetto Graphics a una dimensione specificata in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase::RenderToSize method


Renderizza la forma in un oggetto **Graphics** a una dimensione specificata.

```cpp
float Aspose::Words::Rendering::NodeRendererBase::RenderToSize(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | L'oggetto su cui renderizzare. |
| x | float | La coordinata X (in unità del mondo) dell'angolo superiore sinistro della forma renderizzata. |
| y | float | La coordinata Y (in unità del mondo) dell'angolo superiore sinistro della forma renderizzata. |
| larghezza | float | La larghezza massima (in unità del mondo) che può essere occupata dalla forma renderizzata. |
| altezza | float | L'altezza massima (in unità del mondo) che può essere occupata dalla forma renderizzata. |

### ReturnValue

La scala che è stata calcolata automaticamente per la forma renderizzata per adattarsi alla dimensione specificata.

## Vedi anche

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
