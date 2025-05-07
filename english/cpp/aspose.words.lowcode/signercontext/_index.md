---
title: Aspose::Words::LowCode::SignerContext class
linktitle: SignerContext
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::SignerContext class. Document signer context in C++.'
type: docs
weight: 1334
url: /cpp/aspose.words.lowcode/signercontext/
---
## SignerContext class


[Document](../../aspose.words/document/) signer context.

```cpp
class SignerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Methods

| Method | Description |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | CertificateHolder object with certificate that used to sign file. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | [Font](../../aspose.words/font/) settings used by the processor. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | [Document](../../aspose.words/document/) layout options used by the processor. |
| [get_SignOptions](./get_signoptions/)() const | SignOptions object with various signing options. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warning callback used by the processor. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | CertificateHolder object with certificate that used to sign file. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Font](../../aspose.words/font/) settings used by the processor. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | SignOptions object with various signing options. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Warning callback used by the processor. |
| static [Type](./type/)() |  |
## See Also

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
