---
title: "Aspose::Words::Saving::IFontSavingCallback arayüzü"
linktitle: "IFontSavingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::IFontSavingCallback arayüzü. Bu arayüzü, bir belgeyi C++'ta HTML formatına dışa aktarırken Aspose.Words'un yazı tiplerini nasıl kaydettiğini kontrol etmek ve bildirimler almak istiyorsanız uygulayın."
type: docs
weight: 42000
url: /tr/cpp/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface


Bir belgeyi HTML formatına dışa aktarırken bildirim almak ve Aspose.Words'in yazı tiplerini kaydetme şeklini kontrol etmek istiyorsanız bu arabirimi uygulayın.

```cpp
class IFontSavingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [FontSaving](./fontsaving/)(System::SharedPtr\<Aspose::Words::Saving::FontSavingArgs\>) | Aspose.Words bir yazı tipi kaynağını kaydetmek üzereyken çağrılır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
