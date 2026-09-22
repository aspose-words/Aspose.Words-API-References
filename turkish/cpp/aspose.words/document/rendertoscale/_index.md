---
title: "Aspose::Words::Document::RenderToScale yöntemi"
linktitle: "RenderToScale"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::RenderToScale yöntemi. Belge sayfasını belirtilen ölçeğe göre bir Graphics nesnesine render eder."
type: docs
weight: 70000
url: /tr/cpp/aspose.words/document/rendertoscale/
---
## Document::RenderToScale method


Belge sayfasını belirtilen ölçeğe göre bir **Graphics** nesnesine işler.

```cpp
System::Drawing::SizeF Aspose::Words::Document::RenderToScale(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageIndex | int32_t | 0 tabanlı sayfa indeksi. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | Render edilecek nesne. |
| x | float | Render edilen sayfanın sol üst köşesinin X koordinatı (dünya birimlerinde). |
| y | float | Render edilen sayfanın sol üst köşesinin Y koordinatı (dünya birimlerinde). |
| scale | float | Sayfanın render edilmesi için ölçek (1.0 = %100). |

### ReturnValue

Render edilen sayfanın genişlik ve yüksekliği (dünya birimlerinde).

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
