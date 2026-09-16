---
title: "Aspose::Words::Properties::DocumentPropertyCollection 类"
linktitle: "DocumentPropertyCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::DocumentPropertyCollection 类。BuiltInDocumentProperties 和 CustomDocumentProperties 集合的基类。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class


用于 [BuiltInDocumentProperties](../builtindocumentproperties/) 和 [CustomDocumentProperties](../customdocumentproperties/) 集合的基类。要了解更多信息，请访问 [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) 文档文章。

```cpp
class DocumentPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clear](./clear/)() | 从集合中移除所有属性。 |
| [Contains](./contains/)(const System::String\&) | 如果集合中存在具有指定名称的属性，则返回 **true**。 |
| [get_Count](./get_count/)() | 获取集合中项目的数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个可用于遍历集合中所有项的枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](./idx_get/)(System::String) | 根据属性名称返回一个 [DocumentProperty](../documentproperty/) 对象。 |
| [idx_get](./idx_get/)(int32_t) | 根据索引返回一个 [DocumentProperty](../documentproperty/) 对象。 |
| [IndexOf](./indexof/)(const System::String\&) | 根据名称获取属性的索引。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | 从集合中移除具有指定名称的属性。 |
| [RemoveAt](./removeat/)(int32_t) | 移除指定索引处的属性。 |
| static [Type](./type/)() |  |
## 备注


属性名称不区分大小写。

集合中的属性按名称字母顺序排序。

## 示例



展示如何使用文档的自定义属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// 自定义文档属性是我们可以添加到文档的键值对。
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// 该集合按字母顺序对自定义属性进行排序。
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// 打印文档中的每个自定义属性。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// 使用 DOCPROPERTY 字段显示自定义属性的值。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// 我们可以在 Microsoft Word 中通过 “File” -> “Properties” > “Advanced Properties” > “Custom” 找到这些自定义属性。
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// 以下是从文档中删除自定义属性的三种方法。
// 1 -  按索引删除：
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  按名称删除：
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  一次性清空整个集合：
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## 另见

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
