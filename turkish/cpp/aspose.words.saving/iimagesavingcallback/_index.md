---
title: "Aspose::Words::Saving::IImageSavingCallback arayüzü"
linktitle: "IImageSavingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::IImageSavingCallback arayüzü. Bu arayüzü, bir belge HTML olarak kaydedilirken Aspose.Words'un görüntüleri nasıl kaydettiğini kontrol etmek istiyorsanız uygulayın. C++'ta diğer formatlar tarafından da kullanılabilir."
type: docs
weight: 43000
url: /tr/cpp/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface


Aspose.Words'in bir belgeyi HTML'ye kaydederken görüntüleri kaydetme şeklini kontrol etmek istiyorsanız bu arabirimi uygulayın. Diğer formatlar tarafından da kullanılabilir.

```cpp
class IImageSavingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| virtual [ImageSaving](./imagesaving/)(System::SharedPtr\<Aspose::Words::Saving::ImageSavingArgs\>) | Aspose.Words bir görüntüyü HTML'ye kaydettiğinde çağrılır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
