---
title: "Aspose::Words::Rendering::NodeRendererBase::RenderToScale metodu"
linktitle: "RenderToScale"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::NodeRendererBase::RenderToScale metodu. Şekli C++'da belirtilen ölçeğe bir Graphics nesnesine çizer."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.rendering/noderendererbase/rendertoscale/
---
## NodeRendererBase::RenderToScale method


Şekli belirtilen ölçeğe **Graphics** nesnesine çizer.

```cpp
System::Drawing::SizeF Aspose::Words::Rendering::NodeRendererBase::RenderToScale(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Render edilecek nesne. |
| x | float | Render edilen şeklin sol üst köşesinin X koordinatı (dünya birimlerinde). |
| y | float | Render edilen şeklin sol üst köşesinin Y koordinatı (dünya birimlerinde). |
| scale | float | Şekli render etmek için ölçek (1.0 = %100). |

### ReturnValue

Render edilen şeklin genişliği ve yüksekliği (dünya birimlerinde).

## Ayrıca Bakınız

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
