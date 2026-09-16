---
title: "Aspose::Words::Tables::PreferredWidth::get_Value method"
linktitle: "get_Value"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::PreferredWidth::get_Value 方法。获取首选宽度值。计量单位在 C++ 中的 Type 属性中指定。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.tables/preferredwidth/get_value/
---
## PreferredWidth::get_Value method


获取首选宽度值。计量单位在 [Type](../get_type/) 属性中指定。

```cpp
double Aspose::Words::Tables::PreferredWidth::get_Value() const
```


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

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
