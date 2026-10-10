---
title: "Aspose::Words::Properties::DocumentProperty::ToString 方法"
linktitle: "ToString"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::DocumentProperty::ToString 方法。返回根据当前区域设置格式化的字符串形式的属性值（在 C++ 中）。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty::ToString method


返回属性值为根据当前区域设置格式化的字符串。

```cpp
System::String Aspose::Words::Properties::DocumentProperty::ToString() const override
```

## 备注


将布尔属性转换为 "Y" 或 "N"。将日期属性转换为短日期字符串。对于所有其他类型，使用 Object.ToString() 转换属性。

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


展示自定义文档属性的各种类型转换方法。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

System::DateTime authDate = System::DateTime::get_Today();
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", authDate);
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

ASPOSE_ASSERT_EQ(true, properties->idx_get(u"Authorized")->ToBool());
ASSERT_EQ(u"John Doe", System::ObjectExt::ToString(properties->idx_get(u"Authorized By")));
ASSERT_EQ(authDate, properties->idx_get(u"Authorized Date")->ToDateTime());
ASSERT_EQ(1, properties->idx_get(u"Authorized Revision")->ToInt());
ASPOSE_ASSERT_EQ(123.45, properties->idx_get(u"Authorized Amount")->ToDouble());
```

## 另见

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
