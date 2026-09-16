---
title: "Aspose::Words::BorderType 枚举"
linktitle: "BorderType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BorderType 枚举。指定边框的各侧。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 81000
url: /zh/cpp/aspose.words/bordertype/
---
## BorderType enum


指定边框的各侧。要了解更多信息，请访问 [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) 文档文章。

```cpp
enum class BorderType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | -1 | 默认值。 |
| 底部 | 0 | 指定段落或表格单元格的底部边框。 |
| 左 | 1 | 指定段落或表格单元格的左侧边框。 |
| 右 | 2 | 指定段落或表格单元格的右侧边框。 |
| 顶部 | 3 | 指定段落或表格单元格的顶部边框。 |
| Horizontal | 4 | 指定表格单元格之间或相邻段落之间的水平边框。 |
| Vertical | 5 | 指定表格单元格之间的垂直边框。 |
| DiagonalDown | 6 | 指定表格单元格中的对角线边框。 |
| DiagonalUp | 7 | 指定表格单元格中的对角线边框。 |


## 示例



展示如何插入带有顶部边框的段落。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// 仅在设置了 LineWidth 或 LineStyle 时才设置 ThemeColor。
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
