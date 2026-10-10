---
title: "Aspose::Words::Document::RenderToSize yöntemi"
linktitle: "RenderToSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::RenderToSize yöntemi. Belge sayfasını belirtilen boyuta göre bir Graphics nesnesine render eder (C++)."
type: docs
weight: 71000
url: /tr/cpp/aspose.words/document/rendertosize/
---
## Document::RenderToSize method


Belge sayfasını belirtilen boyuta göre bir **Graphics** nesnesine işler.

```cpp
float Aspose::Words::Document::RenderToSize(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageIndex | int32_t | 0 tabanlı sayfa indeksi. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Render edilecek nesne. |
| x | float | Render edilen sayfanın sol üst köşesinin X koordinatı (dünya birimlerinde). |
| y | float | Render edilen sayfanın sol üst köşesinin Y koordinatı (dünya birimlerinde). |
| genişlik | float | Render edilen sayfanın kaplayabileceği maksimum genişlik (dünya birimlerinde). |
| yükseklik | float | Render edilen sayfanın kaplayabileceği maksimum yükseklik (dünya birimlerinde). |

### ReturnValue

Belirtilen boyuta sığması için render edilen sayfa için otomatik olarak hesaplanan ölçek.

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
