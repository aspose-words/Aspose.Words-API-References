---
title: "Aspose::Words::LowCode::SignerContext classe"
linktitle: "SignerContext"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::SignerContext classe. Contexte de signature de document en C++."
type: docs
weight: 1334
url: /fr/cpp/aspose.words.lowcode/signercontext/
---
## SignerContext class


[Document](../../aspose.words/document/) signer context.

```cpp
class SignerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Objet CertificateHolder avec le certificat utilisé pour signer le fichier. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Paramètres de [Police](../../aspose.words/font/) utilisés par le processeur. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Options de mise en page du [Document](../../aspose.words/document/) utilisées par le processeur. |
| [get_SignOptions](./get_signoptions/)() const | Objet SignOptions avec diverses options de signature. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Rappel d'avertissement utilisé par le processeur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Objet CertificateHolder avec le certificat utilisé pour signer le fichier. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Paramètres de [Police](../../aspose.words/font/) utilisés par le processeur. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Objet SignOptions avec diverses options de signature. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Rappel d'avertissement utilisé par le processeur. |
| static [Type](./type/)() |  |
## Voir aussi

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
