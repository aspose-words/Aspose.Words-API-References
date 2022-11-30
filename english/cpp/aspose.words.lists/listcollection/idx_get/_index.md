---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Gets a list by index.
type: docs
weight: 131
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1");
builder->Writeln(u"Paragraph 2");
builder->Write(u"Paragraph 3");

SharedPtr<NodeCollection> paras = doc->GetChildNodes(NodeType::Paragraph, true);

ASSERT_EQ(0, paras->LINQ_Count([](SharedPtr<Node> n) { return System::DynamicCast<Paragraph>(n)->get_ListFormat()->get_IsListItem(); }));

doc->get_Lists()->Add(ListTemplate::NumberDefault);
SharedPtr<List> list = doc->get_Lists()->idx_get(0);

for (const auto& paragraph : System::IterateOver(paras->LINQ_OfType<SharedPtr<Paragraph>>()))
{
    paragraph->get_ListFormat()->set_List(list);
    paragraph->get_ListFormat()->set_ListLevelNumber(2);
}

ASSERT_EQ(3, paras->LINQ_Count([](SharedPtr<Node> n) { return System::DynamicCast<Paragraph>(n)->get_ListFormat()->get_IsListItem(); }));
```


Shows how to verify owner document properties of lists. 
```cpp
auto doc = MakeObject<Document>();

SharedPtr<ListCollection> lists = doc->get_Lists();

ASPOSE_ASSERT_EQ(doc, lists->get_Document());

SharedPtr<List> list = lists->Add(ListTemplate::BulletDefault);

ASPOSE_ASSERT_EQ(doc, list->get_Document());

std::cout << (String(u"Current list count: ") + lists->get_Count()) << std::endl;
std::cout << (String(u"Is the first document list: ") + (System::ObjectExt::Equals(lists->idx_get(0), list))) << std::endl;
std::cout << (String(u"ListId: ") + list->get_ListId()) << std::endl;
std::cout << (String(u"List is the same by ListId: ") + (System::ObjectExt::Equals(lists->GetListByListId(1), list))) << std::endl;
```

## See Also

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words](../../../)
