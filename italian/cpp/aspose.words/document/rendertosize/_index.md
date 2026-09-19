---
title: "Metodo Aspose::Words::Document::RenderToSize"
linktitle: "RenderToSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::RenderToSize. Renderizza una pagina del documento in un oggetto Graphics a una dimensione specificata in C++."
type: docs
weight: 71000
url: /it/cpp/aspose.words/document/rendertosize/
---
## Document::RenderToSize method


Esegue il rendering di una pagina del documento in un oggetto **Graphics** a una dimensione specificata.

```cpp
float Aspose::Words::Document::RenderToSize(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageIndex | int32_t | L'indice della pagina basato su zero. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | L'oggetto su cui renderizzare. |
| x | float | La coordinata X (in unità di mondo) dell'angolo superiore sinistro della pagina renderizzata. |
| y | float | La coordinata Y (in unità di mondo) dell'angolo superiore sinistro della pagina renderizzata. |
| larghezza | float | La larghezza massima (in unità di mondo) che può essere occupata dalla pagina renderizzata. |
| altezza | float | L'altezza massima (in unità di mondo) che può essere occupata dalla pagina renderizzata. |

### ReturnValue

La scala che è stata calcolata automaticamente per la pagina renderizzata per adattarsi alla dimensione specificata.

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
