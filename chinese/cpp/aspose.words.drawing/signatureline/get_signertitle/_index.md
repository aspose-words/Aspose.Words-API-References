---
title: "Aspose::Words::Drawing::SignatureLine::get_SignerTitle 方法"
linktitle: "get_SignerTitle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::SignatureLine::get_SignerTitle 方法。获取或设置建议的签署人标题（例如，Manager）。此属性在 C++ 中的默认值为空字符串。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.drawing/signatureline/get_signertitle/
---
## SignatureLine::get_SignerTitle method


获取或设置建议签署人的职称（例如，经理）。此属性的默认值为 **empty string**。

```cpp
System::String Aspose::Words::Drawing::SignatureLine::get_SignerTitle()
```


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

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
