---
title: "Aspose::Words::Saving::IResourceSavingCallback interface"
linktitle: "IResourceSavingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::IResourceSavingCallback arayüzü. C++'ta bir belgeyi sabit sayfa HTML veya SVG olarak kaydederken Aspose.Words'un dış kaynakları (görseller, yazı tipleri ve css) nasıl kaydettiğini kontrol etmek istiyorsanız bu arayüzü uygulayın."
type: docs
weight: 45000
url: /tr/cpp/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface


Aspose.Words'in bir belgeyi sabit sayfa HTML veya SVG'ye kaydederken harici kaynakları (görüntüler, yazı tipleri ve css) kaydetme şeklini kontrol etmek istiyorsanız bu arabirimi uygulayın.

```cpp
class IResourceSavingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceSaving](./resourcesaving/)(System::SharedPtr\<Aspose::Words::Saving::ResourceSavingArgs\>) | Aspose.Words dış bir kaynağı sabit sayfa HTML veya SVG formatlarına kaydettiğinde çağrılır. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
