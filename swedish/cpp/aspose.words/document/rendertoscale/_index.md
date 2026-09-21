---
title: "Aspose::Words::Document::RenderToScale method"
linktitle: "RenderToScale"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::RenderToScale method. Renderar en dokumentsida till ett Graphics‑objekt i en angiven skala i C++."
type: docs
weight: 70000
url: /sv/cpp/aspose.words/document/rendertoscale/
---
## Document::RenderToScale method


Renderar en dokumentsida till ett **Graphics**‑objekt i en angiven skala.

```cpp
System::Drawing::SizeF Aspose::Words::Document::RenderToScale(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pageIndex | int32_t | Det 0‑baserade sidindexet. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Objektet att rendera till. |
| x | float | X-koordinaten (i världsenheter) för det övre vänstra hörnet på den renderade sidan. |
| y | float | Y-koordinaten (i världsenheter) för det övre vänstra hörnet på den renderade sidan. |
| skala | float | Skalan för att rendera sidan (1,0 är 100%). |

### ReturnValue

Bredden och höjden (i världsenheter) på den renderade sidan.

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
