---
title: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable yöntemi"
linktitle: "get_IsImageAvailable"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable yöntemi. Geçerli resim C++'ta dışa aktarım için kullanılabilir ise true döndürür."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


Mevcut görüntü dışa aktarmaya uygun ise **true** döndürür.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## Açıklamalar


Belgedeki bazı resimler kullanılabilir olmayabilir; örneğin, resim bağlanmış ve bağlantı erişilemez ya da geçerli bir resme işaret etmiyorsa. Bu durumda Aspose.Words kırmızı çarpı işaretli bir simge dışa aktarır. Bu özellik, orijinal resim kullanılabilir ise **true** döndürür; orijinal resim kullanılabilir değilse **false** döndürür ve kaydetme için bir "no image" simgesi sunulur.

Bir grup şekli veya resim gerektirmeyen bir şekil kaydedilirken bu özellik her zaman **true** olur.

## Ayrıca Bakınız

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
