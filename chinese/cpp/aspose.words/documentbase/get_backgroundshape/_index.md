---
title: "Aspose::Words::DocumentBase::get_BackgroundShape 方法"
linktitle: "get_BackgroundShape"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBase::get_BackgroundShape 方法。获取或设置文档的背景形状。在 C++ 中可以为 null。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/documentbase/get_backgroundshape/
---
## DocumentBase::get_BackgroundShape method


获取或设置文档的背景形状。可以为 **null**。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBase::get_BackgroundShape() const
```

## 备注


Microsoft Word 只允许使用其 [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) 属性等于 [Rectangle](../../../aspose.words.drawing/shapetype/) 的形状作为文档的背景形状。

Microsoft Word 仅支持背景形状的填充属性。所有其他属性均被忽略。

将此属性设置为非 null 值还会将 [DisplayBackgroundShape](../../../aspose.words.settings/viewoptions/get_displaybackgroundshape/) 设置为 **true**。

## 示例



展示如何为文档的每一页设置背景形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_TRUE(System::TestTools::IsNull(doc->get_BackgroundShape()));

// 我们只能使用矩形作为背景形状。
auto shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);

// 有两种方法可以将此形状用作页面背景。
// 1 -  平面颜色：
shapeRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
doc->set_BackgroundShape(shapeRectangle);

doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  图像：
shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shapeRectangle->get_ImageData()->SetImage(get_ImageDir() + u"Transparent background logo.png");

// 调整图像的外观，使其更适合作为水印。
shapeRectangle->get_ImageData()->set_Contrast(0.2);
shapeRectangle->get_ImageData()->set_Brightness(0.7);

doc->set_BackgroundShape(shapeRectangle);

ASSERT_TRUE(doc->get_BackgroundShape()->get_HasImage());

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
saveOptions->set_CacheBackgroundGraphics(false);

// Microsoft Word 不支持将图像作为背景的形状，
// 但我们仍然可以在其他保存格式（例如 .pdf）中看到这些背景。
doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
