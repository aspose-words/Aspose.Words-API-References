---
title: "Aspose::Words::Document::RenderToSize metod"
linktitle: "RenderToSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::RenderToSize metod. Renderar en dokumentsida till ett Graphics-objekt i en angiven storlek i C++."
type: docs
weight: 71000
url: /sv/cpp/aspose.words/document/rendertosize/
---
## Document::RenderToSize method


Ritar en dokumentsida till ett **Graphics**-objekt i en specificerad storlek.

```cpp
float Aspose::Words::Document::RenderToSize(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pageIndex | int32_t | Det 0‑baserade sidindexet. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Objektet att rendera till. |
| x | float | X-koordinaten (i världsenheter) för det övre vänstra hörnet på den renderade sidan. |
| y | float | Y-koordinaten (i världsenheter) för det övre vänstra hörnet på den renderade sidan. |
| bredd | float | Den maximala bredden (i värdenheter) som den renderade sidan kan uppta. |
| höjd | float | Den maximala höjden (i värdenheter) som den renderade sidan kan uppta. |

### ReturnValue

Skalan som automatiskt beräknades för den renderade sidan för att passa den angivna storleken.

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
