---
title: "Aspose::Words::VariableCollection 类"
linktitle: "VariableCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::VariableCollection 类。文档变量的集合。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 73000
url: /zh/cpp/aspose.words/variablecollection/
---
## VariableCollection class


文档变量的集合。要了解更多，请访问 [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) 文档文章。

```cpp
class VariableCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | 向集合中添加文档变量。 |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | 从集合中移除所有元素。 |
| [Contains](./contains/)(const System::String\&) | 确定集合是否包含具有给定名称的文档变量。 |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | 获取集合中包含的元素数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象，可用于遍历集合中的所有变量。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | 获取或设置文档变量，使用不区分大小写的名称。**null** 值不允许作为赋值的右侧，将被替换为空字符串。 |
| [idx_get](./idx_get/)(int32_t) | 获取或设置指定索引处的文档变量。**null** 值不允许作为赋值的右侧，将被替换为空字符串。 |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | 获取或设置文档变量，使用不区分大小写的名称。**null** 值不允许作为赋值的右侧，将被替换为空字符串。 |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | 获取或设置指定索引处的文档变量。**null** 值不允许作为赋值的右侧，将被替换为空字符串。 |
| [IndexOfKey](./indexofkey/)(const System::String\&) | 返回集合中指定文档变量的零基索引。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | 从集合中移除具有指定名称的文档变量。 |
| [RemoveAt](./removeat/)(int32_t) | 移除指定索引处的文档变量。 |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| 类型定义 | 描述 |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## 备注


变量名和变量值都是字符串。

变量名不区分大小写。

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
