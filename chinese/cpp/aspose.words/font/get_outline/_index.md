---
title: "Aspose::Words::Font::get_Outline 方法"
linktitle: "get_Outline"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Outline 方法。若在 C++ 中字体被设置为轮廓，则为 True。"
type: docs
weight: 31000
url: /zh/cpp/aspose.words/font/get_outline/
---
## Font::get_Outline method


如果字体被格式化为轮廓，则为 True。

```cpp
bool Aspose::Words::Font::get_Outline()
```


## 示例



展示如何创建轮廓格式的文本运行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 设置 Outline 标志以将文本的填充颜色更改为白色，并
// 在文本的原始颜色中为每个字符留下细细的轮廓。
builder->get_Font()->set_Outline(true);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has an outline.");

doc->Save(get_ArtifactsDir() + u"Font.Outline.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
