---
title: "Aspose::Words::Properties::DocumentProperty::ToDateTime 方法"
linktitle: "ToDateTime"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::DocumentProperty::ToDateTime 方法。以 UTC 的 DateTime 形式返回属性值（在 C++ 中）。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty::ToDateTime method


返回属性值为 UTC 时间的 **DateTime**。

```cpp
System::DateTime Aspose::Words::Properties::DocumentProperty::ToDateTime()
```

## 备注


如果属性类型不是 [DateTime](../../propertytype/)，则抛出异常。

Microsoft Word 仅为自定义日期属性存储日期部分（不包括时间）。

## 示例



展示如何创建包含日期和时间的自定义文档属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
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
