---
title: "Aspose::Words::Properties::CustomDocumentProperties::Add 方法"
linktitle: "Add"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::CustomDocumentProperties::Add 方法。在 C++ 中创建一个布尔数据类型的新自定义文档属性。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.properties/customdocumentproperties/add/
---
## CustomDocumentProperties::Add(const System::String\&, bool) method


创建一个 [Boolean](../../propertytype/) 数据类型的新自定义文档属性。

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, bool value)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 属性的名称。 |
| value | bool | 属性的值。 |

### ReturnValue

新创建的属性对象。

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

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, const System::String\&) method


创建一个 [String](../../propertytype/) 数据类型的新自定义文档属性。

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, const System::String &value)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 属性的名称。 |
| value | const System::String\& | 属性的值。 |

### ReturnValue

新创建的属性对象。

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

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, double) method


创建一个 [Double](../../propertytype/) 数据类型的新自定义文档属性。

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, double value)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 属性的名称。 |
| value | double | 属性的值。 |

### ReturnValue

新创建的属性对象。

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

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, int32_t) method


创建一个 [Number](../../propertytype/) 数据类型的新自定义文档属性。

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, int32_t value)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 属性的名称。 |
| value | int32_t | 属性的值。 |

### ReturnValue

新创建的属性对象。

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

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## CustomDocumentProperties::Add(const System::String\&, System::DateTime) method


创建一个 [DateTime](../../propertytype/) 数据类型的新自定义文档属性。

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::Add(const System::String &name, System::DateTime value)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 属性的名称。 |
| value | System::DateTime | 属性的值。 |

### ReturnValue

新创建的属性对象。

## 示例



展示如何创建包含日期和时间的自定义文档属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```


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

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
