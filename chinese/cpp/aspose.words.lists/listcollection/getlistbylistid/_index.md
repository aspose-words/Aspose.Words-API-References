---
title: "Aspose::Words::Lists::ListCollection::GetListByListId method"
linktitle: "GetListByListId"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListCollection::GetListByListId method. 通过列表标识符在 C++ 中获取列表。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection::GetListByListId method


通过列表标识符获取列表。

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::GetListByListId(int32_t listId)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| listId | int32_t | 列表标识符。 |

### ReturnValue

返回列表对象。如果未找到具有指定标识符的列表，则返回 **null**。
## 备注


通常情况下您不需要使用此方法。大多数情况下，您只需设置 [List](../../listformat/get_list/) 属性的 [ListFormat](../../listformat/) 对象，即可对段落应用列表格式。

## 示例



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
