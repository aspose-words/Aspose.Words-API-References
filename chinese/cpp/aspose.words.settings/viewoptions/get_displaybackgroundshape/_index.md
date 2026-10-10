---
title: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape 方法"
linktitle: "get_DisplayBackgroundShape"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape 方法。控制在 C++ 中打印布局视图的背景形状显示。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.settings/viewoptions/get_displaybackgroundshape/
---
## ViewOptions::get_DisplayBackgroundShape method


控制打印布局视图中背景形状的显示。

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape() const
```


## 示例



展示如何在视图选项中隐藏/显示文档背景图像。
```cpp
// 使用 HTML 字符串创建一个具有纯色背景的新文档。
const System::String html = u"<html>\r\n                <body style='background-color: blue'>\r\n                    <p>Hello world!</p>\r\n                </body>\r\n            </html>";

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_Unicode()->GetBytes(html)));

// 文档的来源具有纯色背景，
// 其存在将把 "DisplayBackgroundShape" 标志设置为 "true"。
ASSERT_TRUE(doc->get_ViewOptions()->get_DisplayBackgroundShape());

// 将 "DisplayBackgroundShape" 保持为 "true" 以使文档显示背景颜色。
// 这可能会影响某些文本颜色以提升可见性。
// 将 "DisplayBackgroundShape" 设置为 "false" 以不显示背景颜色。
doc->get_ViewOptions()->set_DisplayBackgroundShape(displayBackgroundShape);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayBackgroundShape.docx");
```

## 另见

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
