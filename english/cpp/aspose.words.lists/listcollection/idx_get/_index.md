---
title: Aspose::Words::Lists::ListCollection::idx_get method
linktitle: idx_get
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListCollection::idx_get method. Gets a list by index in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.lists/listcollection/idx_get/
---
## ListCollection::idx_get method


Gets a list by index.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::idx_get(int32_t index)
```


## Examples



Shows how to apply list formatting of an existing list to a collection of paragraphs. 
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


Shows how to verify owner document properties of lists. 
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

## See Also

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
