---
title: "Aspose::Words::Rendering::NodeRendererBase::RenderToScale‑metod"
linktitle: "RenderToScale"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Rendering::NodeRendererBase::RenderToScale‑metod. Renderar formen till ett Graphics‑objekt i en angiven skala i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.rendering/noderendererbase/rendertoscale/
---
## NodeRendererBase::RenderToScale method


Renderar formen till ett **Graphics**-objekt med en angiven skala.

```cpp
System::Drawing::SizeF Aspose::Words::Rendering::NodeRendererBase::RenderToScale(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Objektet att rendera till. |
| x | float | X‑koordinaten (i världsenheter) för det övre vänstra hörnet av den renderade formen. |
| y | float | Y‑koordinaten (i världsenheter) för det övre vänstra hörnet av den renderade formen. |
| skala | float | Skalan för rendering av formen (1,0 är 100 %). |

### ReturnValue

Bredden och höjden (i världsenheter) för den renderade formen.

## Se även

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
