---
title: "Aspose::Words::Tables::PreferredWidthType 枚举"
linktitle: "PreferredWidthType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::PreferredWidthType 枚举。指定表格或单元格在 C++ 中首选宽度的计量单位。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


指定表格或单元格首选宽度的计量单位。

```cpp
enum class PreferredWidthType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 自动 | 1 | 未指定首选宽度。表格或单元格的实际宽度要么使用显式宽度指定，要么在表格显示时根据表格自动适应设置由表格布局算法自动确定。 |
| 百分比 | 2 | 使用指定的百分比测量当前项的宽度。 |
| 磅 | 3 | 使用指定的点数（1/72 英寸）测量当前项的宽度。 |


## 示例



展示如何验证表格单元格的首选宽度类型和数值。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## 另见

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
