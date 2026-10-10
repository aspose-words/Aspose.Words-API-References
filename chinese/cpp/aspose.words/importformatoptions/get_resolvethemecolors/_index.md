---
title: "Aspose::Words::ImportFormatOptions::get_ResolveThemeColors 方法"
linktitle: "get_ResolveThemeColors"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatOptions::get_ResolveThemeColors 方法。获取或设置一个布尔值，指定是否强制解析形状的主题颜色。默认值在 C++ 中为 false。"
type: docs
weight: 8500
url: /zh/cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


获取或设置一个布尔值，指定是否强制解析形状的主题颜色。默认值为 **false**。

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## 备注


请注意，此选项仅在 [KeepSourceFormatting](../../importformatmode/) 模式下相关。

通常情况下，Aspose.Words 在导入时不会解析源主题颜色，因为可以在不将格式属性展开为直接属性的情况下保留样式。然而，在这种情况下，导入的形状的实际颜色可能与原始文档中的颜色不同。原因是源文档和目标文档的主题颜色不同。将此选项设置为 **true** 将强制解析源形状的主题颜色，从而保留它们在源文档中的实际颜色。

## 示例



展示如何在导入节点时解析形状的源主题颜色。
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// 移动到主页脚并插入使用主题颜色的形状。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// 将源页脚导入到目标文档，并解析主题颜色，
// 因此形状保留来自源文档的实际颜色。
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## 另见

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
