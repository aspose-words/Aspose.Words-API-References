---
title: "Aspose::Words::Loading::IResourceLoadingCallback interface"
linktitle: "IResourceLoadingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::IResourceLoadingCallback interface. Bu arayüzü, C++'da bir belgeyi içe aktarırken ve DocumentBuilder kullanarak resim eklerken Aspose.Words'un harici kaynağı nasıl yüklediğini kontrol etmek istiyorsanız uygulayın."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface


Bu arayüzü, [DocumentBuilder](../../aspose.words/documentbuilder/) kullanarak resim eklerken Aspose.Words'un harici kaynağı nasıl yüklediğini kontrol etmek istiyorsanız uygulayın.

```cpp
class IResourceLoadingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceLoading](./resourceloading/)(System::SharedPtr\<Aspose::Words::Loading::ResourceLoadingArgs\>) | Aspose.Words herhangi bir harici kaynağı yüklediğinde çağrılır. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
