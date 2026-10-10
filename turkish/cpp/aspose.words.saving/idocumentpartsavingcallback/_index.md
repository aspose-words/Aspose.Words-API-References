---
title: "Aspose::Words::Saving::IDocumentPartSavingCallback interface"
linktitle: "IDocumentPartSavingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::IDocumentPartSavingCallback arayüzü. Bu arayüzü, bir belgeyi Html veya Epub formatına C++'ta dışa aktarırken Aspose.Words'in belge bölümlerini nasıl kaydettiğini kontrol etmek ve bildirimler almak istiyorsanız uygulayın."
type: docs
weight: 40000
url: /tr/cpp/aspose.words.saving/idocumentpartsavingcallback/
---
## IDocumentPartSavingCallback interface


Bu arayüzü, bir belgeyi [Html](../../aspose.words/saveformat/) veya [Epub](../../aspose.words/saveformat/) formatına dışa aktarırken Aspose.Words'in belge bölümlerini nasıl kaydettiğini kontrol etmek ve bildirimler almak istiyorsanız uygulayın.

```cpp
class IDocumentPartSavingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [DocumentPartSaving](./documentpartsaving/)(System::SharedPtr\<Aspose::Words::Saving::DocumentPartSavingArgs\>) | Aspose.Words bir belge bölümünü kaydetmek üzereyken çağrılır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
