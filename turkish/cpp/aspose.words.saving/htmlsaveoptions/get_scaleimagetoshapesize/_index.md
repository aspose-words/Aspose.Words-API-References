---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize method"
linktitle: "get_ScaleImageToShapeSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize yöntemi. Görüntülerin HTML, MHTML veya EPUB'a aktarılırken Aspose.Words tarafından sınırlayıcı şekil boyutuna ölçeklenip ölçeklenmeyeceğini belirtir. Varsayılan değer C++'da true'dur."
type: docs
weight: 46000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


HTML, MHTML veya EPUB'a dışa aktarırken görüntülerin Aspose.Words tarafından sınırlayıcı şekil boyutuna ölçeklenip ölçeklenmeyeceğini belirtir. Varsayılan değer **true**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## Açıklamalar


Microsoft Word belgesindeki bir görüntü bir şekildir. Şeklin bir boyutu vardır ve görüntünün kendi boyutu vardır. Bu boyutlar doğrudan bağlı değildir. Örneğin, görüntü 1024x786 piksel olabilir, ancak bu görüntüyü gösteren şekil 400x300 puan olabilir.

Bir görüntüyü tarayıcıda göstermek için, şekil boyutuna ölçeklenmesi gerekir. [ScaleImageToShapeSize](./) özelliği, görüntünün ölçeklemesinin nerede gerçekleşeceğini kontrol eder: HTML'ye aktarım sırasında Aspose.Words içinde mi yoksa belgeyi görüntülerken tarayıcıda mı.

[ScaleImageToShapeSize](./) **true** olduğunda, görüntü HTML'ye aktarım sırasında [Aspose.Words](../../../aspose.words/) tarafından yüksek kaliteli ölçekleme ile ölçeklenir. [ScaleImageToShapeSize](./) **false** olduğunda, görüntü orijinal boyutuyla çıktılanır ve tarayıcının ölçeklemesi gerekir.

Genel olarak, tarayıcılar hızlı ve düşük kaliteli ölçekleme yapar. Sonuç olarak, [ScaleImageToShapeSize](./) **true** olduğunda tarayıcıda genellikle daha iyi görüntü kalitesi ve daha küçük dosya boyutu elde edersiniz, ancak **false** olduğunda daha iyi baskı kalitesi ve daha hızlı dönüşüm elde edersiniz.

Bireysel raster görüntüler içeren şekillere ek olarak, bu seçenek raster görüntülerden oluşan grup şekilleri de etkiler. Eğer [ScaleImageToShapeSize](./) **false** ise ve bir grup şekil, içsel çözünürlüğü [ImageResolution](../get_imageresolution/) içinde belirtilen değerden daha yüksek raster görüntüler içeriyorsa, Aspose.Words o grup için render çözünürlüğünü artıracaktır. Bu, HTML'ye kaydederken gruplanmış yüksek çözünürlüklü görüntülerin kalitesinin daha iyi korunmasını sağlar.

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
