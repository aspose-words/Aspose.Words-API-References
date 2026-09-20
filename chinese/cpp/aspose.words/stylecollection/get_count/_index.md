---
title: "Aspose::Words::StyleCollection::get_Count 方法"
linktitle: "get_Count"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::StyleCollection::get_Count 方法。获取 C++ 中集合中样式的数量。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/stylecollection/get_count/
---
## StyleCollection::get_Count method


获取集合中样式的数量。

```cpp
int32_t Aspose::Words::StyleCollection::get_Count()
```


## 示例



展示如何向文档的样式集合添加一个 [Style](../../style/)。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// 为我们以后可能添加到此集合的新样式设置默认参数。
styles->get_DefaultFont()->set_Name(u"Courier New");
// 如果我们添加一个 \"StyleType.Paragraph\" 类型的样式，集合将应用这些值。
// 其 \"DefaultParagraphFormat\" 属性到样式的 \"ParagraphFormat\" 属性。
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// 添加一个样式，然后验证它具有默认设置。
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## 另见

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
