---
title: "Aspose::Words::LowCode::SignerContext class"
linktitle: "SignerContext"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::SignerContext class. Контекст подписания документа в C++."
type: docs
weight: 1334
url: /ru/cpp/aspose.words.lowcode/signercontext/
---
## SignerContext class


[Document](../../aspose.words/document/) signer context.

```cpp
class SignerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Объект CertificateHolder с сертификатом, используемым для подписи файла. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Настройки [Font](../../aspose.words/font/) используемые процессором. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Параметры макета [Document](../../aspose.words/document/) используемые процессором. |
| [get_SignOptions](./get_signoptions/)() const | Объект SignOptions с различными параметрами подписи. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Обратный вызов предупреждения, используемый процессором. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Объект CertificateHolder с сертификатом, используемым для подписи файла. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Настройки [Font](../../aspose.words/font/) используемые процессором. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Объект SignOptions с различными параметрами подписи. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Обратный вызов предупреждения, используемый процессором. |
| static [Type](./type/)() |  |
## См. также

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
