---
title: "Aspose::Words::Saving::MetafileRenderingMode enum"
linktitle: "MetafileRenderingMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MetafileRenderingMode enum. Aspose.Words'un C++'ta WMF ve EMF metafillerini nasıl işlemesi gerektiğini belirtir."
type: docs
weight: 69000
url: /tr/cpp/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enum


Aspose.Words'in WMF ve EMF meta dosyalarını nasıl işlemesi gerektiğini belirtir.

```cpp
enum class MetafileRenderingMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| VectorWithFallback | 0 | Aspose.Words, bir metafili vektör grafiği olarak işlemeye çalışır. Eğer Aspose.Words bazı metafil kayıtlarını vektör grafiğine doğru şekilde işleyemezse, bu metafili bitmap olarak işler. |
| Vector | 1 | Aspose.Words bir metafili vektör grafiği olarak render eder. |
| Bitmap | 2 | Aspose.Words, bir metafili bitmap'e renderlemek için GDI+ çağırır ve ardından bitmap'i çıktı belgesine kaydeder. |

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
