---
title: "Aspose::Words::Tables::PreferredWidth::get_Type method"
linktitle: "get_Type"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::PreferredWidth::get_Type 方法。获取在 C++ 中用于此首选宽度值的计量单位。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.tables/preferredwidth/get_type/
---
## PreferredWidth::get_Type method


获取此首选宽度值使用的计量单位。

```cpp
Aspose::Words::Tables::PreferredWidthType Aspose::Words::Tables::PreferredWidth::get_Type() const
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

* Enum [PreferredWidthType](../../preferredwidthtype/)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
