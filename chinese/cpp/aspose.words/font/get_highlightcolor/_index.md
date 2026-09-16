---
title: "Aspose::Words::Font::get_HighlightColor 方法"
linktitle: "get_HighlightColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_HighlightColor 方法。获取或设置 C++ 中的高亮（标记）颜色。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words/font/get_highlightcolor/
---
## Font::get_HighlightColor method


获取或设置突出显示（标记）颜色。

```cpp
System::Drawing::Color Aspose::Words::Font::get_HighlightColor()
```


## 示例



展示如何使用其字体属性格式化文本运行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
