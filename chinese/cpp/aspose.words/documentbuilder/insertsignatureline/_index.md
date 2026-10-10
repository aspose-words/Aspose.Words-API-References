---
title: "Aspose::Words::DocumentBuilder::InsertSignatureLine 方法"
linktitle: "InsertSignatureLine"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertSignatureLine 方法。 在 C++ 中在当前位置插入签名行。"
type: docs
weight: 46000
url: /zh/cpp/aspose.words/documentbuilder/insertsignatureline/
---
## DocumentBuilder::InsertSignatureLine(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) method


在当前位置插入签名行。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertSignatureLine(const System::SharedPtr<Aspose::Words::SignatureLineOptions> &signatureLineOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| signatureLineOptions | const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\& | 存储创建签名行参数的对象。 |

### ReturnValue

刚刚插入的签名行节点。

## 示例



展示如何使用个人证书和签名行对文档进行签署。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto signatureLineOptions = System::MakeObject<Aspose::Words::SignatureLineOptions>();
signatureLineOptions->set_Signer(u"vderyushev");
signatureLineOptions->set_SignerTitle(u"QA");
signatureLineOptions->set_Email(u"vderyushev@aspose.com");
signatureLineOptions->set_ShowDate(true);
signatureLineOptions->set_DefaultInstructions(false);
signatureLineOptions->set_Instructions(u"Please sign here.");
signatureLineOptions->set_AllowComments(true);

System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = builder->InsertSignatureLine(signatureLineOptions)->get_SignatureLine();
signatureLine->set_ProviderId(System::Guid::Parse(u"CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

ASSERT_FALSE(signatureLine->get_IsSigned());
ASSERT_FALSE(signatureLine->get_IsValid());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignatureLineId(signatureLine->get_Id());
signOptions->set_ProviderId(signatureLine->get_ProviderId());
signOptions->set_Comments(u"Document was signed by vderyushev");
signOptions->set_SignTime(System::DateTime::get_Now());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx", get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// 重新打开我们保存的文档，并验证 \"IsSigned\" 和 \"IsValid\" 属性均等于 \"true\",
// 这表明签名行包含签名。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [SignatureLineOptions](../../signaturelineoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertSignatureLine(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) method


在指定位置插入签名行。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertSignatureLine(const System::SharedPtr<Aspose::Words::SignatureLineOptions> &signatureLineOptions, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, Aspose::Words::Drawing::WrapType wrapType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| signatureLineOptions | const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\& | 存储创建签名行参数的对象。 |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | 指定测量签名线距离的起点。 |
| left | double | 从原点到签名线左侧的距离（点）。 |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | 指定测量签名线距离的起点。 |
| top | double | 从原点到签名线顶部的距离（点）。 |
| wrapType | Aspose::Words::Drawing::WrapType | 指定文本环绕签名线的方式。 |

### ReturnValue

刚刚插入的签名行节点。
## 备注


您可以使用此方法返回的 [Shape](../../../aspose.words.drawing/shape/) 对象更改图像大小、位置、定位方式以及其他设置。

## 示例



展示如何在文档中插入内联签名行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Manager");
options->set_Email(u"johndoe@aspose.com");
options->set_ShowDate(true);
options->set_DefaultInstructions(false);
options->set_Instructions(u"Please sign here.");
options->set_AllowComments(true);

builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 2.0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 3.0, Aspose::Words::Drawing::WrapType::Inline);

// 在 Microsoft Word 中可以通过双击签名行进行签署。
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineInline.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [SignatureLineOptions](../../signaturelineoptions/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
