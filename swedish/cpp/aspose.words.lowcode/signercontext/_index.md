---
title: "Aspose::Words::LowCode::SignerContext klass"
linktitle: "SignerContext"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::SignerContext klass. Dokument‑signaturkontext i C++."
type: docs
weight: 1334
url: /sv/cpp/aspose.words.lowcode/signercontext/
---
## SignerContext class


[Document](../../aspose.words/document/) signer context.

```cpp
class SignerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | CertificateHolder‑objekt med certifikat som används för att signera filen. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | [Font](../../aspose.words/font/) inställningar som används av processorn. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | [Document](../../aspose.words/document/) layoutalternativ som används av processorn. |
| [get_SignOptions](./get_signoptions/)() const | SignOptions‑objekt med olika signeringsalternativ. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Varningscallback som används av processorn. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | CertificateHolder‑objekt med certifikat som används för att signera filen. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Font](../../aspose.words/font/) inställningar som används av processorn. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | SignOptions‑objekt med olika signeringsalternativ. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Varningscallback som används av processorn. |
| static [Type](./type/)() |  |
## Se även

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
