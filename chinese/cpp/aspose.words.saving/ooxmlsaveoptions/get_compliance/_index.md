---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance 方法"
linktitle: "get_Compliance"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance 方法。指定输出文档的 OOXML 版本。默认值为 Ecma376_2006（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/ooxmlsaveoptions/get_compliance/
---
## OoxmlSaveOptions::get_Compliance method


指定输出文档的 OOXML 版本。默认值为 [Ecma376_2006](../../ooxmlcompliance/)。

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance()
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


展示如何配置列表在每个章节重新编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// \"IsRestartAtEachSection\" 属性仅在以下情况下适用
// 文档的 OOXML 合规级别高于 \"OoxmlComplianceCore.Ecma376\" 标准。
auto options = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
options->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

builder->get_ListFormat()->set_List(list);

builder->Writeln(u"List item 1");
builder->Writeln(u"List item 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"List item 3");
builder->Writeln(u"List item 4");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx");

ASPOSE_ASSERT_EQ(restartListAtEachSection, doc->get_Lists()->idx_get(0)->get_IsRestartAtEachSection());
```


展示如何向文档插入 DML 形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是形状可能具有的两种环绕类型。
// 1 -  浮动：
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  行内：
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// 如果您需要创建 \"non-primitive\" 形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
// TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded 或 DiagonalCornersRounded，
// 那么请使用 \"Strict\" 或 \"Transitional\" 合规性保存文档，这允许将形状保存为 DML。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## 另见

* Enum [OoxmlCompliance](../../ooxmlcompliance/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
