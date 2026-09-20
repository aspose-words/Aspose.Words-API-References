---
title: "Aspose::Words::HeightRule 枚举"
linktitle: "HeightRule"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::HeightRule 枚举。指定在 C++ 中确定对象高度的规则。"
type: docs
weight: 91000
url: /zh/cpp/aspose.words/heightrule/
---
## HeightRule enum


指定确定对象高度的规则。

```cpp
enum class HeightRule
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| AtLeast | 0 | 高度至少为指定的磅值。如果需要，它会增长以容纳对象内的所有文本。 |
| Exactly | 1 | 高度以磅为单位精确指定。请注意，如果文本无法适应此高度的对象，它将被截断。 |
| 自动 | 2 | 高度将自动增长以容纳对象内的所有文本。 |


## 示例



展示如何使用文档生成器格式化行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// 开始第二行，然后配置其高度。生成器将把这些设置应用于
// 它当前的行，以及随后创建的任何新行。
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// 第一行未受到填充重新配置的影响，仍保留默认值。
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
