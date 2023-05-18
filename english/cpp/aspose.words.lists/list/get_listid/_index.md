---
title: Aspose::Words::Lists::List::get_ListId method
linktitle: get_ListId
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::List::get_ListId method. Gets the unique identifier of the list in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.lists/list/get_listid/
---
## List::get_ListId method


Gets the unique identifier of the list.

```cpp
int32_t Aspose::Words::Lists::List::get_ListId() const
```

## Remarks


You do not normally need to use this property. But if you use it, you normally do so in conjunction with the [GetListByListId()](../../listcollection/getlistbylistid/) method to find a list by its identifier.

## Examples



Shows how to output all paragraphs in a document that are list items. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Bulleted list item 1");
builder->Writeln(u"Bulleted list item 2");
builder->Writeln(u"Bulleted list item 3");
builder->get_ListFormat()->RemoveNumbers();

SharedPtr<NodeCollection> paras = doc->GetChildNodes(NodeType::Paragraph, true);

for (auto para : System::IterateOver(
         paras->LINQ_OfType<SharedPtr<Paragraph>>()->LINQ_Where([](SharedPtr<Paragraph> p) { return p->get_ListFormat()->get_IsListItem(); })))
{
    std::cout << String::Format(u"This paragraph belongs to list ID# {0}, number style \"{1}\"", para->get_ListFormat()->get_List()->get_ListId(),
                                para->get_ListFormat()->get_ListLevel()->get_NumberStyle())
              << std::endl;
    std::cout << "\t\"" << para->GetText().Trim() << "\"" << std::endl;
}
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

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
