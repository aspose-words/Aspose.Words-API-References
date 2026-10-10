---
title: "Aspose::Words::Properties::DocumentProperty::get_Value 方法"
linktitle: "get_Value"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::DocumentProperty::get_Value 方法。获取或设置属性的值（在 C++ 中）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.properties/documentproperty/get_value/
---
## DocumentProperty::get_Value method


获取或设置属性的值。

```cpp
System::SharedPtr<System::Object> Aspose::Words::Properties::DocumentProperty::get_Value()
```

## 备注


不能为 **null**。

## 示例



展示如何使用内置文档属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// “Document” 对象在其成员中包含部分元数据。
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// 文档还在其内置属性中存储元数据。
// 每个内置属性都是文档的 “BuiltInDocumentProperties” 对象的成员。
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // 某些属性可能存储多个值。
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << System::String::Format(u"\tValue:\t\"{0}\"", value) << std::endl;
        }
    }
    else
    {
        std::cout << System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()) << std::endl;
    }
}
```

## 另见

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
