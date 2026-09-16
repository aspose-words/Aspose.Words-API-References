---
title: "Aspose::Words::Drawing::SignatureLine 类"
linktitle: "SignatureLine"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::SignatureLine 类。提供对签名行属性的访问。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.drawing/signatureline/
---
## SignatureLine class


提供对签名行属性的访问。要了解更多信息，请访问 [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) 文档文章。

```cpp
class SignatureLine : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() | 获取或设置一个值，指示签署人在签名对话框中是否可以添加评论。此属性的默认值为 **false**。 |
| [get_DefaultInstructions](./get_defaultinstructions/)() | 获取或设置一个值，指示在签名对话框中是否显示默认说明。此属性的默认值为 **true**。 |
| [get_Email](./get_email/)() | 获取或设置建议的签署人电子邮件地址。此属性的默认值为 **empty string**。 |
| [get_Id](./get_id/)() | 获取或设置此签名行的标识符。使用 [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/) 对文档进行签名时，可以将此标识符与数字签名关联。该值必须唯一，默认情况下会随机生成新的 Guid (**NewGuid**)。 |
| [get_Instructions](./get_instructions/)() | 获取或设置在签署签名行时显示给签署人的指示。如果已设置 [DefaultInstructions](./get_defaultinstructions/)，则此属性会被忽略。此属性的默认值为 **empty string**。 |
| [get_IsSigned](./get_issigned/)() | 指示签名行已由数字签名签署。 |
| [get_IsValid](./get_isvalid/)() | 指示签名行已由数字签名签署且该数字签名有效。 |
| [get_ProviderId](./get_providerid/)() | 获取或设置此签名行的签名提供程序标识符。默认值为 "{00000000-0000-0000-0000-000000000000}"。 |
| [get_ShowDate](./get_showdate/)() | 获取或设置一个值，指示签名行中是否显示签署日期。此属性的默认值为 **true**。 |
| [get_Signer](./get_signer/)() | 获取或设置签名行的建议签署人。此属性的默认值为 **empty string**。 |
| [get_SignerTitle](./get_signertitle/)() | 获取或设置建议签署人的职称（例如，经理）。此属性的默认值为 **empty string**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | 用于 [Aspose::Words::Drawing::SignatureLine::get_AllowComments](./get_allowcomments/) 的设置器。 |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | 用于 [Aspose::Words::Drawing::SignatureLine::get_DefaultInstructions](./get_defaultinstructions/) 的设置器。 |
| [set_Email](./set_email/)(const System::String\&) | 用于 [Aspose::Words::Drawing::SignatureLine::get_Email](./get_email/) 的设置器。 |
| [set_Id](./set_id/)(System::Guid) | 用于 [Aspose::Words::Drawing::SignatureLine::get_Id](./get_id/) 的设置器。 |
| [set_Instructions](./set_instructions/)(const System::String\&) | 用于 [Aspose::Words::Drawing::SignatureLine::get_Instructions](./get_instructions/) 的设置器。 |
| [set_ProviderId](./set_providerid/)(System::Guid) | 用于 [Aspose::Words::Drawing::SignatureLine::get_ProviderId](./get_providerid/) 的设置器。 |
| [set_ShowDate](./set_showdate/)(bool) | 用于设置 [Aspose::Words::Drawing::SignatureLine::get_ShowDate](./get_showdate/) 的 setter。 |
| [set_Signer](./set_signer/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::SignatureLine::get_Signer](./get_signer/) 的 setter。 |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::SignatureLine::get_SignerTitle](./get_signertitle/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何创建签名线并将其插入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_AllowComments(true);
options->set_DefaultInstructions(true);
options->set_Email(u"john.doe@management.com");
options->set_Instructions(u"Please sign here");
options->set_ShowDate(true);
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Senior Manager");

// 插入一个将包含签名线的形状，其外观我们将
// 使用我们上面创建的 "SignatureLineOptions" 对象进行自定义。
// 如果我们插入的形状坐标起始于页面的右下角，
// 我们需要提供负的 x 和 y 坐标以将形状显示出来。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// 通过其 Shape 对象验证我们的签名线属性。
System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = shape->get_SignatureLine();

ASSERT_EQ(u"john.doe@management.com", signatureLine->get_Email());
ASSERT_EQ(u"John Doe", signatureLine->get_Signer());
ASSERT_EQ(u"Senior Manager", signatureLine->get_SignerTitle());
ASSERT_EQ(u"Please sign here", signatureLine->get_Instructions());
ASSERT_TRUE(signatureLine->get_ShowDate());
ASSERT_TRUE(signatureLine->get_AllowComments());
ASSERT_TRUE(signatureLine->get_DefaultInstructions());

doc->Save(get_ArtifactsDir() + u"Shape.SignatureLine.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
