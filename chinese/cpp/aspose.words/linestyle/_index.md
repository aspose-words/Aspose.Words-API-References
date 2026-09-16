---
title: "Aspose::Words::LineStyle 枚举"
linktitle: "LineStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LineStyle 枚举。指定 C++ 中 Border 的线条样式。"
type: docs
weight: 96000
url: /zh/cpp/aspose.words/linestyle/
---
## LineStyle enum


指定 [Border](../border/) 的线条样式。

```cpp
enum class LineStyle
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 |  |
| 单线 | 1 |  |
| 粗线 | 2 |  |
| 双线 | 3 |  |
| Hairline | 5 |  |
| Dot | 6 |  |
| DashLargeGap | 7 |  |
| 点划线 | 8 |  |
| DotDotDash | 9 |  |
| Triple | 10 |  |
| ThinThickSmallGap | 11 |  |
| ThickThinSmallGap | 12 |  |
| ThinThickThinSmallGap | 13 |  |
| ThinThickMediumGap | 14 |  |
| ThickThinMediumGap | 15 |  |
| ThinThickThinMediumGap | 16 |  |
| ThinThickLargeGap | 17 |  |
| ThickThinLargeGap | 18 |  |
| ThinThickThinLargeGap | 19 |  |
| Wave | 20 |  |
| DoubleWave | 21 |  |
| DashSmallGap | 22 |  |
| DashDotStroker | 23 |  |
| Emboss3D | 24 |  |
| Engrave3D | 25 |  |
| Outset | 26 |  |
| Inset | 27 |  |


## 示例



展示如何在文档中插入被边框包围的字符串。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
