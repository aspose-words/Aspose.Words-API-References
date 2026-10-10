---
title: "Aspose::Words::Settings::ViewOptions 类"
linktitle: "ViewOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::ViewOptions 类。提供各种选项以控制文档在 Microsoft Word 中的显示方式。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.settings/viewoptions/
---
## ViewOptions class


提供各种选项，以控制文档在 Microsoft Word 中的显示方式。欲了解更多，请访问 [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/cpp/work-with-word-document-options-and-appearance/) 文档文章。

```cpp
class ViewOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayBackgroundShape](./get_displaybackgroundshape/)() const | 控制打印布局视图中背景形状的显示。 |
| [get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)() const | 关闭文本顶部与页面上边缘之间空间的显示。 |
| [get_FormsDesign](./get_formsdesign/)() const | 指定文档是否处于表单设计模式。 |
| [get_ViewType](./get_viewtype/)() const | 控制 Microsoft Word 中的视图模式。 |
| [get_ZoomPercent](./get_zoompercent/)() const | 获取或设置查看文档的百分比。 |
| [get_ZoomType](./get_zoomtype/)() const | 获取或设置基于窗口大小的缩放值。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayBackgroundShape](./set_displaybackgroundshape/)(bool) | 用于设置 [Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape](./get_displaybackgroundshape/)。 |
| [set_DoNotDisplayPageBoundaries](./set_donotdisplaypageboundaries/)(bool) | 用于设置 [Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)。 |
| [set_FormsDesign](./set_formsdesign/)(bool) | 用于设置 [Aspose::Words::Settings::ViewOptions::get_FormsDesign](./get_formsdesign/)。 |
| [set_ViewType](./set_viewtype/)(Aspose::Words::Settings::ViewType) | 用于设置 [Aspose::Words::Settings::ViewOptions::get_ViewType](./get_viewtype/)。 |
| [set_ZoomPercent](./set_zoompercent/)(int32_t) | 用于设置 [Aspose::Words::Settings::ViewOptions::get_ZoomPercent](./get_zoompercent/)。 |
| [set_ZoomType](./set_zoomtype/)(Aspose::Words::Settings::ZoomType) | 用于设置 [Aspose::Words::Settings::ViewOptions::get_ZoomType](./get_zoomtype/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何设置自定义缩放比例，旧版本的 Microsoft Word 在加载文档时会应用该比例。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```


展示如何设置自定义缩放类型，旧版本的 Microsoft Word 在加载文档时会应用该设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// 将 "ZoomType" 属性设置为 "ZoomType.PageWidth" 以获取 Microsoft Word
// 以自动缩放文档以适应页面宽度。
// 将 "ZoomType" 属性设置为 "ZoomType.FullPage" 以获取 Microsoft Word
// 以自动缩放文档，使整个首页可见。
// 将 "ZoomType" 属性设置为 "ZoomType.TextFit" 以获取 Microsoft Word
// 以自动缩放文档以适应首页内部文本边距。
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
