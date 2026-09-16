---
title: "Aspose::Words::Properties::DocumentPropertyCollection::get_Count 方法"
linktitle: "get_Count"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::DocumentPropertyCollection::get_Count 方法。获取集合中项目的数量（C++）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.properties/documentpropertycollection/get_count/
---
## DocumentPropertyCollection::get_Count method


获取集合中项目的数量。

```cpp
int32_t Aspose::Words::Properties::DocumentPropertyCollection::get_Count()
```


## 示例



展示如何使用自定义文档属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// 每个文档都包含一组自定义属性，这些属性与内置属性一样，都是键值对。
// 文档具有固定的内置属性列表。用户创建所有自定义属性。
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```

## 另见

* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
