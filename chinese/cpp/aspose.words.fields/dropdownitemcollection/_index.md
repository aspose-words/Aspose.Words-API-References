---
title: "Aspose::Words::Fields::DropDownItemCollection 类"
linktitle: "DropDownItemCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::DropDownItemCollection 类。表示下拉表单字段中所有项目的字符串集合。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class


表示下拉表单字段中所有项目的字符串集合。要了解更多，请访问[Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/)文档文章。

```cpp
class DropDownItemCollection : public System::Collections::Generic::IEnumerable<System::String>,
                               public Aspose::Words::IComplexAttr
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::String\&) | 在集合末尾添加一个字符串。 |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | 从集合中移除所有元素。 |
| [Contains](./contains/)(const System::String\&) | 确定集合是否包含指定的值。 |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | 获取集合中包含的元素数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个可用于遍历集合中所有项的枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 获取或设置指定索引处的元素。 |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | 获取或设置指定索引处的元素。 |
| [IndexOf](./indexof/)(const System::String\&) | 返回集合中指定值的零基索引。 |
| [Insert](./insert/)(int32_t, const System::String\&) | 在指定索引处向集合插入一个字符串。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | 从集合中移除指定的值。 |
| [RemoveAt](./removeat/)(int32_t) | 在指定索引处移除一个值。 |
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

## 示例



展示如何插入组合框字段并编辑其项目集合中的元素。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入组合框，然后验证其下拉项目集合。
// 在 Microsoft Word 中，用户将点击组合框，
// 然后选择集合中要显示的文本项之一。
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// 有两种方法向现有下拉框项集合添加新项。
// 1 - 将项追加到集合的末尾：
dropDownItems->Add(u"Four");

// 2 - 在指定索引处将项插入到另一个项之前：
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// 遍历集合并打印每个元素。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// 有两种方法从下拉项集合中移除元素。
// 1 - 移除内容等于给定字符串的项：
dropDownItems->Remove(u"Four");

// 2 - 移除指定索引处的项：
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// 清空整个下拉项集合。
dropDownItems->Clear();
```

## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
