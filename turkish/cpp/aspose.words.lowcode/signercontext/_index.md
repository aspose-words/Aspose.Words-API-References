---
title: "Aspose::Words::LowCode::SignerContext sınıfı"
linktitle: "SignerContext"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::SignerContext sınıfı. C++'da belge imzalayan bağlam."
type: docs
weight: 1334
url: /tr/cpp/aspose.words.lowcode/signercontext/
---
## SignerContext class


[Document](../../aspose.words/document/) signer context.

```cpp
class SignerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Dosyayı imzalamak için kullanılan sertifikaya sahip CertificateHolder nesnesi. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | İşlemci tarafından kullanılan [Font](../../aspose.words/font/) ayarları. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | İşlemci tarafından kullanılan [Document](../../aspose.words/document/) düzen seçenekleri. |
| [get_SignOptions](./get_signoptions/)() const | Çeşitli imzalama seçeneklerine sahip SignOptions nesnesi. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | İşlemci tarafından kullanılan uyarı geri çağrısı. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Dosyayı imzalamak için kullanılan sertifikaya sahip CertificateHolder nesnesi. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | İşlemci tarafından kullanılan [Font](../../aspose.words/font/) ayarları. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Çeşitli imzalama seçeneklerine sahip SignOptions nesnesi. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | İşlemci tarafından kullanılan uyarı geri çağrısı. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
