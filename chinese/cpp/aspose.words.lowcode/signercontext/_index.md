---
title: "Aspose::Words::LowCode::SignerContext 类"
linktitle: "SignerContext"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::SignerContext 类。C++ 中的文档签名者上下文。"
type: docs
weight: 1334
url: /zh/cpp/aspose.words.lowcode/signercontext/
---
## SignerContext class


[Document](../../aspose.words/document/) signer context.

```cpp
class SignerContext : public Aspose::Words::LowCode::ProcessorContext
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | CertificateHolder 对象，包含用于签署文件的证书。 |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | 处理器使用的 [Font](../../aspose.words/font/) 设置。 |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | 处理器使用的 [Document](../../aspose.words/document/) 布局选项。 |
| [get_SignOptions](./get_signoptions/)() const | SignOptions 对象，包含各种签名选项。 |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | 处理器使用的警告回调。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | CertificateHolder 对象，包含用于签署文件的证书。 |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | 处理器使用的 [Font](../../aspose.words/font/) 设置。 |
| [set_SignOptions](./set_signoptions/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | SignOptions 对象，包含各种签名选项。 |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 处理器使用的警告回调。 |
| static [Type](./type/)() |  |
## 另见

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
