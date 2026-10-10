---
title: "Aspose::Words::Fields::DropDownItemCollection::Insert 方法"
linktitle: "Insert"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::DropDownItemCollection::Insert 方法。 在 C++ 中将字符串插入集合的指定索引位置。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.fields/dropdownitemcollection/insert/
---
## DropDownItemCollection::Insert method


在指定索引处向集合插入一个字符串。

```cpp
void Aspose::Words::Fields::DropDownItemCollection::Insert(int32_t index, const System::String &value)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 插入值的零基索引。 |
| value | const System::String\& | 要插入的字符串。 |

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

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
