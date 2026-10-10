---
title: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize method"
linktitle: "RenderToSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize method. Renderar formen till ett Graphics-objekt i en specificerad storlek i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase::RenderToSize method


Renderar formen till ett **Graphics**-objekt med en angiven storlek.

```cpp
float Aspose::Words::Rendering::NodeRendererBase::RenderToSize(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Objektet att rendera till. |
| x | float | X‑koordinaten (i världsenheter) för det övre vänstra hörnet av den renderade formen. |
| y | float | Y‑koordinaten (i världsenheter) för det övre vänstra hörnet av den renderade formen. |
| bredd | float | Den maximala bredden (i värdenheter) som kan tas upp av den renderade formen. |
| höjd | float | Den maximala höjden (i värdenheter) som kan tas upp av den renderade formen. |

### ReturnValue

Skalan som automatiskt beräknades för den renderade formen för att passa den angivna storleken.

## Se även

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
