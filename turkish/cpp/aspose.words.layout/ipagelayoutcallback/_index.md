---
title: "Aspose::Words::Layout::IPageLayoutCallback arayüzü"
linktitle: "IPageLayoutCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::IPageLayoutCallback arayüzü. Bu arayüzü, C++'da sayfa yerleşim modeli oluşturma ve renderleme sırasında çağrılan kendi özel metodunuzu oluşturmak istiyorsanız uygulayın."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface


Sayfa düzeni modelinin oluşturulması ve render edilmesi sırasında çağrılan kendi özel yönteminizi istiyorsanız bu arabirimi uygulayın.

```cpp
class IPageLayoutCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Layout::PageLayoutCallbackArgs\>) | Bu, yerleşim oluşturma ve renderleme ilerlemesi hakkında bildirim yapmak için çağrılır. |
| static [Type](./type/)() |  |
## Açıklamalar


Bu arayüzün temel kullanımı, uygulama kodunun oluşturma sürecini iptal etmesine izin vermektir.

Belgenin başında yalnızca birkaç sayfa için sayfa yerleşim modeli oluşturmak, ardından süreci iptal edip sadece zaten oluşturulmuş olanı renderlemek mümkündür.

Ancak, sürecin tamamlanmış olsaydı her sayfa için renderlenecek olanla render sonuçlarının eşleşmeyebileceğini unutmayın.

Bu teknik her belge için çalışmayabilir veya tamamen başarısız olabilir.

## Ayrıca Bakınız

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
