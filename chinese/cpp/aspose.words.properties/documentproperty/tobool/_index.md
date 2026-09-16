---
title: "Aspose::Words::Properties::DocumentProperty::ToBool 方法"
linktitle: "ToBool"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::DocumentProperty::ToBool 方法。返回属性值为 C++ 中的 bool 类型。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty::ToBool method


以 bool 形式返回属性值。

```cpp
bool Aspose::Words::Properties::DocumentProperty::ToBool()
```

## 备注


如果属性类型不是 [Boolean](../../propertytype/) 则抛出异常。

## 示例



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
