---
title: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize metodu"
linktitle: "RenderToSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize metodu. Şekli belirtilen boyuta bir Graphics nesnesine C++'da render eder."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase::RenderToSize method


Şekli belirtilen boyuta **Graphics** nesnesine çizer.

```cpp
float Aspose::Words::Rendering::NodeRendererBase::RenderToSize(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Render edilecek nesne. |
| x | float | Render edilen şeklin sol üst köşesinin X koordinatı (dünya birimlerinde). |
| y | float | Render edilen şeklin sol üst köşesinin Y koordinatı (dünya birimlerinde). |
| genişlik | float | Render edilen şeklin kaplayabileceği maksimum genişlik (dünya birimlerinde). |
| yükseklik | float | Render edilen şeklin kaplayabileceği maksimum yükseklik (dünya birimlerinde). |

### ReturnValue

Belirtilen boyuta uyması için render edilen şekil için otomatik olarak hesaplanan ölçek.

## Ayrıca Bakınız

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
