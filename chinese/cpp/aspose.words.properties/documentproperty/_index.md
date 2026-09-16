---
title: "Aspose::Words::Properties::DocumentProperty 类"
linktitle: "DocumentProperty"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::DocumentProperty 类。表示自定义或内置文档属性。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.properties/documentproperty/
---
## DocumentProperty class


表示自定义或内置文档属性。要了解更多信息，请访问 [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) 文档文章。

```cpp
class DocumentProperty : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_IsLinkToContent](./get_islinktocontent/)() | 显示此属性是否链接到内容。 |
| [get_LinkSource](./get_linksource/)() const | 获取已链接自定义文档属性的来源。 |
| [get_Name](./get_name/)() const | 返回属性的名称。 |
| [get_Type](./get_type/)() const | 获取属性的数据类型。 |
| [get_Value](./get_value/)() | 获取或设置属性的值。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(const System::SharedPtr\<System::Object\>\&) | 用于设置 [Aspose::Words::Properties::DocumentProperty::get_Value](./get_value/) 的 setter。 |
| [ToBool](./tobool/)() | 以 bool 形式返回属性值。 |
| [ToByteArray](./tobytearray/)() | 返回属性值为字节数组。 |
| [ToDateTime](./todatetime/)() | 返回属性值为 UTC 时间的 **DateTime**。 |
| [ToDouble](./todouble/)() | 返回属性值为 double。 |
| [ToInt](./toint/)() | 返回属性值为整数。 |
| [ToString](./tostring/)() const override | 返回属性值为根据当前区域设置格式化的字符串。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
