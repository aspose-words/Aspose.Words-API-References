---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream yöntemi"
linktitle: "get_ImageStream"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream yöntemi. Resmin C++'ta kaydedileceği akışı belirtmenizi sağlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs::get_ImageStream method


Görüntünün kaydedileceği akışı belirtmeye izin verir.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```

## Açıklamalar


Bu özellik, HTML sırasında dosyalar yerine akışlara resim kaydetmenizi sağlar.

Varsayılan değer **null**'dır. Bu özellik **null** olduğunda, resim [ImageFileName](../get_imagefilename/) özelliğinde belirtilen bir dosyaya kaydedilir.

[IImageSavingCallback](../../iimagesavingcallback/) kullanarak bir resmi başka bir resimle değiştiremezsiniz. Bu yalnızca resimlerin kaydedileceği konumu kontrol etmek için tasarlanmıştır.

## Ayrıca Bakınız

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
