---
title: "Aspose::Words::Document::get_CustomDocumentProperties 方法"
linktitle: "get_CustomDocumentProperties"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_CustomDocumentProperties 方法。返回一个集合，表示文档中所有自定义文档属性（C++）。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words/document/get_customdocumentproperties/
---
## Document::get_CustomDocumentProperties method


返回表示文档所有自定义属性的集合。

```cpp
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> Aspose::Words::Document::get_CustomDocumentProperties()
```


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

* Class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
