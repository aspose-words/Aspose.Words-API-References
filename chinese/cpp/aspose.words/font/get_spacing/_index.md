---
title: "Aspose::Words::Font::get_Spacing 方法"
linktitle: "get_Spacing"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Spacing 方法。返回或设置字符之间的间距（以点为单位），在 C++ 中。"
type: docs
weight: 40000
url: /zh/cpp/aspose.words/font/get_spacing/
---
## Font::get_Spacing method


返回或设置字符之间的间距（以点为单位）。

```cpp
double Aspose::Words::Font::get_Spacing()
```


## 示例



展示如何设置字符的水平缩放和间距。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 添加一段文本并将字符宽度增加到 150%。
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// 添加文本运行，并在每个字符之间添加 1pt 的额外水平间距。
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// 添加文本运行，并将字符间距缩小 1pt。
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(get_ArtifactsDir() + u"Font.ScalingSpacing.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
