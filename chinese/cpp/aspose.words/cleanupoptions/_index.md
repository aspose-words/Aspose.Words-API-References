---
title: "Aspose::Words::CleanupOptions 类"
linktitle: "CleanupOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CleanupOptions 类。允许指定文档清理的选项。要了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/cleanupoptions/
---
## CleanupOptions class


允许为文档清理指定选项。欲了解更多，请访问[文档清理指南](https://docs.aspose.com/words/cpp/clean-up-a-document/)文档文章。

```cpp
class CleanupOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [CleanupOptions](./cleanupoptions/)() |  |
| [get_DuplicateStyle](./get_duplicatestyle/)() const | 获取/设置一个标志，指示是否应从文档中删除重复样式。默认值为 **false**。 |
| [get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/)() const | 指定应从文档中删除未使用的 [BuiltIn](../style/get_builtin/) 样式。 |
| [get_UnusedLists](./get_unusedlists/)() const | 指定是否应从文档中删除未使用的列表及列表定义。默认值为 **true**。 |
| [get_UnusedStyles](./get_unusedstyles/)() const | 指定是否应从文档中删除未使用的样式。默认值为 **true**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DuplicateStyle](./set_duplicatestyle/)(bool) | 用于设置 [Aspose::Words::CleanupOptions::get_DuplicateStyle](./get_duplicatestyle/) 的 setter。 |
| [set_UnusedBuiltinStyles](./set_unusedbuiltinstyles/)(bool) | 用于设置 [Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/) 的 setter。 |
| [set_UnusedLists](./set_unusedlists/)(bool) | 用于设置 [Aspose::Words::CleanupOptions::get_UnusedLists](./get_unusedlists/) 的 setter。 |
| [set_UnusedStyles](./set_unusedstyles/)(bool) | 用于设置 [Aspose::Words::CleanupOptions::get_UnusedStyles](./get_unusedstyles/) 的 setter。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
