---
title: "Aspose::Words::LowCode::SignerContext clase"
linktitle: "SignerContext"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LowCode::SignerContext clase. Contexto de firmante de documento en C++."
type: docs
weight: 1334
url: /es/cpp/aspose.words.lowcode/signercontext/
---
## SignerContext class


[Document](../../aspose.words/document/) signer context.

```cpp
class SignerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Objeto CertificateHolder con certificado que se utiliza para firmar el archivo. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Configuraciones de [Fuente](../../aspose.words/font/) usadas por el procesador. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Opciones de diseño de [Documento](../../aspose.words/document/) usadas por el procesador. |
| [get_SignOptions](./get_signoptions/)() const | Objeto SignOptions con varias opciones de firma. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Función de devolución de llamada de advertencia usada por el procesador. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Objeto CertificateHolder con certificado que se utiliza para firmar el archivo. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Configuraciones de [Fuente](../../aspose.words/font/) usadas por el procesador. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Objeto SignOptions con varias opciones de firma. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Función de devolución de llamada de advertencia usada por el procesador. |
| static [Type](./type/)() |  |
## Ver también

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
