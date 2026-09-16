---
title: "Aspose::Words::CleanupOptions::get_UnusedStyles 方法"
linktitle: "get_UnusedStyles"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CleanupOptions::get_UnusedStyles 方法。指定是否应从文档中删除未使用的样式。默认值在 C++ 中为 true。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/cleanupoptions/get_unusedstyles/
---
## CleanupOptions::get_UnusedStyles method


指定是否应从文档中删除未使用的样式。默认值为 **true**。

```cpp
bool Aspose::Words::CleanupOptions::get_UnusedStyles() const
```


## 示例



展示如何从文档中删除所有未使用的自定义样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// 结合内置样式，文档现在有八种样式。
// 只要文档中有任何使用该样式的文本，自定义样式就会被标记为“已使用”。
// 以该样式格式化。这意味着我们添加的 4 种样式目前未被使用。
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// 应用自定义字符样式，然后应用自定义列表样式。这样会将它们标记为“已使用”。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

// 现在，有一个未使用的字符样式和一个未使用的列表样式。
// 当使用 CleanupOptions 对象配置时，Cleanup() 方法可以针对未使用的样式并将其删除。
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_UnusedLists(true);
cleanupOptions->set_UnusedStyles(true);
cleanupOptions->set_UnusedBuiltinStyles(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// 删除所有应用了自定义样式的节点会再次将其标记为“未使用”。
// 重新运行 Cleanup 方法以将其删除。
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup(cleanupOptions);

ASSERT_EQ(2, doc->get_Styles()->get_Count());
```

## 另见

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
