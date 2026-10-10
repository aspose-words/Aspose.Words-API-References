---
title: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor 方法"
linktitle: "OptimizeFor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor 方法。允许将文档内容以及默认的 Aspose.Words 行为优化到特定版本的 MS Word。使用此方法可防止在加载文档时 MS Word 显示 \\\"Compatibility mode\\\" 功能区。（注意，您可能还需要将 Compliance 属性设置为 Iso29500_2008_Transitional 或更高版本。）在 C++ 中。"
type: docs
weight: 75000
url: /zh/cpp/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions::OptimizeFor method


允许将文档内容以及默认的 Aspose.Words 行为优化到特定版本的 MS Word。使用此方法可防止在加载文档时 MS Word 显示 \"Compatibility mode\" 功能区。（注意，您可能还需要将 [Compliance](../../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) 属性设置为 [Iso29500_2008_Transitional](../../../aspose.words.saving/ooxmlcompliance/) 或更高版本。）

```cpp
void Aspose::Words::Settings::CompatibilityOptions::OptimizeFor(Aspose::Words::Settings::MsWordVersion version)
```


## 示例



展示如何为已保存的文档设置 OOXML 合规规范以遵循。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 如果我们将兼容性选项配置为符合 Microsoft Word 2003，
// 插入图像将使用 VML 定义其形状。
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// "ISO/IEC 29500:2008" OOXML 标准不支持 VML 形状。
// 如果我们将 SaveOptions 对象的 \"Compliance\" 属性设置为 \"OoxmlCompliance.Iso29500_2008_Strict\",
// 任何在传递此对象时保存的文档都必须遵循该标准。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// 我们保存的文档使用 DML 定义形状，以符合 \"ISO/IEC 29500:2008\" OOXML 标准。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


展示如何垂直对齐文本框的文本内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// 将 "VerticalAnchor" 属性设置为 "TextBoxAnchor.Top" 以
// 使此文本框中的文本与形状的顶部对齐。
// 将 "VerticalAnchor" 属性设置为 "TextBoxAnchor.Middle" 以
// 使此文本框中的文本居中于形状。
// 将 "VerticalAnchor" 属性设置为 "TextBoxAnchor.Bottom" 以
// 使此文本框中的文本与形状的底部对齐。
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// 从 Microsoft Word 2007 起，文本框内文本的垂直对齐功能可用。
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## 另见

* Enum [MsWordVersion](../../mswordversion/)
* Class [CompatibilityOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
