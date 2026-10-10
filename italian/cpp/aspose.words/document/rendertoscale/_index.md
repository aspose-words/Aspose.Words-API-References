---
title: "Metodo Aspose::Words::Document::RenderToScale"
linktitle: "RenderToScale"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::RenderToScale. Renderizza una pagina del documento in un oggetto Graphics a una scala specificata in C++."
type: docs
weight: 70000
url: /it/cpp/aspose.words/document/rendertoscale/
---
## Document::RenderToScale method


Esegue il rendering di una pagina del documento in un oggetto **Graphics** a una scala specificata.

```cpp
System::Drawing::SizeF Aspose::Words::Document::RenderToScale(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageIndex | int32_t | L'indice della pagina basato su zero. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | L'oggetto su cui renderizzare. |
| x | float | La coordinata X (in unità di mondo) dell'angolo superiore sinistro della pagina renderizzata. |
| y | float | La coordinata Y (in unità di mondo) dell'angolo superiore sinistro della pagina renderizzata. |
| scale | float | La scala per il rendering della pagina (1.0 è 100%). |

### ReturnValue

La larghezza e l'altezza (in unità di mondo) della pagina renderizzata.

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
