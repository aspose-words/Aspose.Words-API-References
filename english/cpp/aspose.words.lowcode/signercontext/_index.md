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


Document signer context

```cpp
class SignerContext : public ProcessorContext
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_CertificateHolder](./get_certificateholder/)() const | CertificateHolder object with certificate that used to sign file. |
| [get_SignOptions](./get_signoptions/)() const | SignOptions object with various signing options. |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\> \&) | CertificateHolder object with certificate that used to sign file. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\> \&) | SignOptions object with various signing options. |
| [GetType](../processorcontext/gettype/)() const override |  |
| [Is](../processorcontext/is/)(const System::TypeInfo \&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| static [Type](../processorcontext/type/)() |  |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Font settings used by the processor. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Document layout options used by the processor. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warning callback used by the processor. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\> \&) | Font settings used by the processor. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\> \&) | Warning callback used by the processor. |
## See Also

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
