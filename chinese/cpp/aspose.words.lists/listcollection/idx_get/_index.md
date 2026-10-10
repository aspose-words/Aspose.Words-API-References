---
title: "Aspose::Words::Lists::ListCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListCollection::idx_get 方法。根据索引获取列表（C++）。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.lists/listcollection/idx_get/
---
## ListCollection::idx_get method


通过索引获取列表。

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::idx_get(int32_t index)
```


## 示例



展示如何将现有列表的列表格式应用于一组段落。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1");
builder->Writeln(u"Paragraph 2");
builder->Write(u"Paragraph 3");

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

ASSERT_EQ(0, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);

for (auto&& paragraph : System::IterateOver(paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    paragraph->get_ListFormat()->set_List(list);
    paragraph->get_ListFormat()->set_ListLevelNumber(2);
}

ASSERT_EQ(3, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));
```


展示如何验证列表的所属文档属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::ListCollection> lists = doc->get_Lists();
ASPOSE_ASSERT_EQ(doc, lists->get_Document());

System::SharedPtr<Aspose::Words::Lists::List> list = lists->Add(Aspose::Words::Lists::ListTemplate::BulletDefault);
ASPOSE_ASSERT_EQ(doc, list->get_Document());

std::cout << (System::String(u"Current list count: ") + lists->get_Count()) << std::endl;
std::cout << (System::String(u"Is the first document list: ") + (System::ObjectExt::Equals(lists->idx_get(0), list))) << std::endl;
std::cout << (System::String(u"ListId: ") + list->get_ListId()) << std::endl;
std::cout << (System::String(u"List is the same by ListId: ") + (System::ObjectExt::Equals(lists->GetListByListId(1), list))) << std::endl;
```

## 另见

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
