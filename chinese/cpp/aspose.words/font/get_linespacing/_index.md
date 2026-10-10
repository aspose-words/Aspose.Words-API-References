---
title: "Aspose::Words::Font::get_LineSpacing 方法"
linktitle: "get_LineSpacing"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_LineSpacing 方法。返回此字体的行间距（以点为单位），在 C++ 中。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words/font/get_linespacing/
---
## Font::get_LineSpacing method


返回此字体的行间距（以磅为单位）。

```cpp
double Aspose::Words::Font::get_LineSpacing()
```


## 示例



展示如何获取字体的行间距（单位：点）。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 为 DocumentBuilder 设置不同的字体并验证它们的行间距。
builder->get_Font()->set_Name(u"Calibri");
ASPOSE_ASSERT_EQ(14.6484375, builder->get_Font()->get_LineSpacing());

builder->get_Font()->set_Name(u"Times New Roman");
ASPOSE_ASSERT_EQ(13.798828125, builder->get_Font()->get_LineSpacing());
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
