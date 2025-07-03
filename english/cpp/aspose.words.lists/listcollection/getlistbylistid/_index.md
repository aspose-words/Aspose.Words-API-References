---
title: Aspose::Words::Lists::ListCollection::GetListByListId method
linktitle: GetListByListId
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListCollection::GetListByListId method. Gets a list by a list identifier in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection::GetListByListId method


Gets a list by a list identifier.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::GetListByListId(int32_t listId)
```


| Parameter | Type | Description |
| --- | --- | --- |
| listId | int32_t | The list identifier. |

### ReturnValue

Returns the list object. Returns **null** if a list with the specified identifier was not found.
## Remarks


You don't normally need to use this method. Most of the time you apply list formatting to paragraphs just by settings the [List](../../listformat/get_list/) property of the [ListFormat](../../listformat/) object.

## Examples



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
