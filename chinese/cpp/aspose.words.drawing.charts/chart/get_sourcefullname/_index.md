---
title: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName 方法"
linktitle: "get_SourceFullName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName 方法。在 C++ 中获取此图表链接的 xls/xlsx 文件的路径和名称。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.drawing.charts/chart/get_sourcefullname/
---
## Chart::get_SourceFullName method


获取此图表所链接的 xls/xlsx 文件的路径和名称。

```cpp
System::String Aspose::Words::Drawing::Charts::Chart::get_SourceFullName()
```


## 示例



展示如何在图表已链接时获取/设置外部 xls/xlsx 文档的完整名称。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::String sourceFullName = shape->get_Chart()->get_SourceFullName();
ASSERT_TRUE(sourceFullName.Contains(u"Examples\\Data\\Spreadsheet.xlsx"));
```

## 另见

* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
