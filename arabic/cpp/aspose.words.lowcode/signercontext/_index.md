---
title: "فئة Aspose::Words::LowCode::SignerContext"
linktitle: "SignerContext"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::LowCode::SignerContext. سياق موقّع المستند في C++."
type: docs
weight: 1334
url: /ar/cpp/aspose.words.lowcode/signercontext/
---
## SignerContext class


[Document](../../aspose.words/document/) signer context.

```cpp
class SignerContext : public Aspose::Words::LowCode::ProcessorContext
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | كائن CertificateHolder مع شهادة تُستخدم لتوقيع الملف. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | إعدادات [الخط](../../aspose.words/font/) المستخدمة بواسطة المعالج. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | خيارات تخطيط [المستند](../../aspose.words/document/) المستخدمة بواسطة المعالج. |
| [get_SignOptions](./get_signoptions/)() const | كائن SignOptions مع خيارات توقيع متنوعة. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | استدعاء التحذير المستخدم بواسطة المعالج. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | كائن CertificateHolder مع شهادة تُستخدم لتوقيع الملف. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | إعدادات [الخط](../../aspose.words/font/) المستخدمة بواسطة المعالج. |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | كائن SignOptions مع خيارات توقيع متنوعة. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | استدعاء التحذير المستخدم بواسطة المعالج. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
