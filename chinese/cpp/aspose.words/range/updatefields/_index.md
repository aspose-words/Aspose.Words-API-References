---
title: "Aspose::Words::Range::UpdateFields method"
linktitle: "UpdateFields"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Range::UpdateFields method. 更新此范围内文档字段的值（C++）。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words/range/updatefields/
---
## Range::UpdateFields method


更新此范围内文档字段的值。

```cpp
void Aspose::Words::Range::UpdateFields()
```

## 备注


当您打开、修改然后保存文档时，Aspose.Words 不会自动更新字段，它会保持原样。因此，如果您以编程方式修改了文档并希望确保保存的文档中出现正确（已计算）的字段值，通常需要在保存之前调用此方法。

执行邮件合并后无需更新字段，因为邮件合并本身是一种字段更新，会自动更新文档中的所有字段。

此方法并未更新所有字段类型。有关受支持字段类型的详细列表，请参阅程序员指南。

此方法不会更新与页面布局算法相关的字段（例如 PAGE、PAGES、PAGEREF）。当您渲染文档或调用 [UpdatePageLayout](../../document/updatepagelayout/) 时，页面布局相关的字段会被更新。

要更新整个文档中的字段，请使用 [UpdateFields](../../document/updatefields/)。

## 示例



展示如何更新范围内的所有字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DOCPROPERTY Category");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->InsertField(u" DOCPROPERTY Category");

// 上述 DOCPROPERTY 字段将显示此内置文档属性的值。
doc->get_BuiltInDocumentProperties()->set_Category(u"MyCategory");

// 如果我们更新文档属性的值，则需要更新所有 DOCPROPERTY 字段以显示它。
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// 更新第一节范围内的所有字段。
doc->get_FirstSection()->get_Range()->UpdateFields();

ASSERT_EQ(u"MyCategory", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
```

## 另见

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
