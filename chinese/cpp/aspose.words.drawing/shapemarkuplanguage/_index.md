---
title: "Aspose::Words::Drawing::ShapeMarkupLanguage 枚举"
linktitle: "ShapeMarkupLanguage"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeMarkupLanguage enum。指定在 C++ 中用于形状的 Markup 语言。"
type: docs
weight: 37000
url: /zh/cpp/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enum


指定用于形状的 [Markup](../../aspose.words.markup/) 语言。

```cpp
enum class ShapeMarkupLanguage : uint8_t
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Dml | 0 | [Drawing](../)[Markup](../../aspose.words.markup/) 语言用于定义形状。 |
| Vml | 1 | 矢量 [Markup](../../aspose.words.markup/) 语言用于定义形状。 |


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

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
