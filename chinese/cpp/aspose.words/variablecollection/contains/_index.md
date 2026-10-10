---
title: "Aspose::Words::VariableCollection::Contains 方法"
linktitle: "Contains"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::VariableCollection::Contains 方法。确定集合是否在 C++ 中包含具有给定名称的文档变量。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/variablecollection/contains/
---
## VariableCollection::Contains method


确定集合是否包含具有给定名称的文档变量。

```cpp
bool Aspose::Words::VariableCollection::Contains(const System::String &name)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 要定位的文档变量的大小写不敏感名称。 |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.

## 示例



展示如何使用文档的变量集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// 每个文档都有一个键/值对变量的集合，我们可以向其中添加项目。
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// 我们可以使用 DOCVARIABLE 字段在文档正文中显示变量的值。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// 为现有键分配值将会更新它们。
variables->Add(u"Home address", u"456 Queen St.");

// 随后我们必须更新 DOCVARIABLE 字段，以确保它们显示最新的值。
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// 验证具有特定名称或值的文档变量是否存在。
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// 变量集合会自动按名称对变量进行字母顺序排序。
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// 遍历变量集合。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// 以下是从集合中删除文档变量的三种方法。
// 1 -  按名称：
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  按索引：
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  一次性清除整个集合：
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## 另见

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
