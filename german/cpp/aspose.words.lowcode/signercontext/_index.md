---
title: "Aspose::Words::LowCode::SignerContext Klasse"
linktitle: "SignerContext"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::SignerContext Klasse. Dokumentenunterzeichner-Kontext in C++."
type: docs
weight: 1334
url: /de/cpp/aspose.words.lowcode/signercontext/
---
## SignerContext class


[Document](../../aspose.words/document/) signer context.

```cpp
class SignerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | CertificateHolder-Objekt mit Zertifikat, das zum Signieren der Datei verwendet wird. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | [Font](../../aspose.words/font/) Einstellungen, die vom Prozessor verwendet werden. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | [Document](../../aspose.words/document/) Layout-Optionen, die vom Prozessor verwendet werden. |
| [get_SignOptions](./get_signoptions/)() const | SignOptions-Objekt mit verschiedenen Signieroptionen. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warnungs-Callback, der vom Prozessor verwendet wird. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | CertificateHolder-Objekt mit Zertifikat, das zum Signieren der Datei verwendet wird. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Font](../../aspose.words/font/) Einstellungen, die vom Prozessor verwendet werden. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | SignOptions-Objekt mit verschiedenen Signieroptionen. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Warnungs-Callback, der vom Prozessor verwendet wird. |
| static [Type](./type/)() |  |
## Siehe auch

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
