---
title: "Aspose::Words::LowCode::ComparerContext sınıfı"
linktitle: "ComparerContext"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::ComparerContext sınıfı. C++'ta belge karşılaştırıcı bağlamı."
type: docs
weight: 550
url: /tr/cpp/aspose.words.lowcode/comparercontext/
---
## ComparerContext class


[Document](../../aspose.words/document/) comparer context.

```cpp
class ComparerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ComparerContext](./comparercontext/)() |  |
| [get_AcceptRevisions](./get_acceptrevisions/)() const | Karşılaştırmadan önce belgelerdeki revizyonların kabul edilip edilmediğini gösterir. Karşılaştırılan belgeler revizyon içeriyorsa ve bu bayrak false olarak ayarlanmışsa, işlemci revizyonları reddeder. Varsayılan değer **true**. |
| [get_Author](./get_author/)() const | Belge karşılaştırması sırasında oluşturulan revizyonlara atanacak yazar. |
| [get_CompareOptions](./get_compareoptions/)() const | Belgeler karşılaştırılırken kullanılan seçenekler. |
| [get_DateTime](./get_datetime/)() const | Belge karşılaştırması sırasında oluşturulan revizyonlara atanan tarih ve saat. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | İşlemci tarafından kullanılan [Font](../../aspose.words/font/) ayarları. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | İşlemci tarafından kullanılan [Document](../../aspose.words/document/) düzen seçenekleri. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | İşlemci tarafından kullanılan uyarı geri çağrısı. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_AcceptRevisions](./set_acceptrevisions/)(bool) | Karşılaştırmadan önce belgelerdeki revizyonların kabul edilip edilmediğini gösterir. Karşılaştırılan belgeler revizyon içeriyorsa ve bu bayrak false olarak ayarlanmışsa, işlemci revizyonları reddeder. Varsayılan değer **true**. |
| [set_Author](./set_author/)(const System::String\&) | Belge karşılaştırması sırasında oluşturulan revizyonlara atanacak yazar. |
| [set_DateTime](./set_datetime/)(System::DateTime) | Belge karşılaştırması sırasında oluşturulan revizyonlara atanan tarih ve saat. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | İşlemci tarafından kullanılan [Font](../../aspose.words/font/) ayarları. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | İşlemci tarafından kullanılan uyarı geri çağrısı. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
