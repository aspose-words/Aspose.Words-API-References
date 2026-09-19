---
title: "classe Aspose::Words::LowCode::SignerContext"
linktitle: "SignerContext"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::LowCode::SignerContext. Contesto del firmatario del documento in C++."
type: docs
weight: 1334
url: /it/cpp/aspose.words.lowcode/signercontext/
---
## SignerContext class


[Document](../../aspose.words/document/) signer context.

```cpp
class SignerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Oggetto CertificateHolder con certificato utilizzato per firmare il file. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Impostazioni [Font](../../aspose.words/font/) utilizzate dal processore. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Opzioni di layout [Document](../../aspose.words/document/) utilizzate dal processore. |
| [get_SignOptions](./get_signoptions/)() const | Oggetto SignOptions con varie opzioni di firma. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Callback di avviso utilizzato dal processore. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Oggetto CertificateHolder con certificato utilizzato per firmare il file. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Impostazioni [Font](../../aspose.words/font/) utilizzate dal processore. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Oggetto SignOptions con varie opzioni di firma. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Callback di avviso utilizzato dal processore. |
| static [Type](./type/)() |  |
## Vedi anche

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
