---
title: "Aspose::Words::Bibliography::PersonCollection::Contains 方法"
linktitle: "Contains"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Bibliography::PersonCollection::Contains 方法。 在 C++ 中确定集合是否包含特定人员。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.bibliography/personcollection/contains/
---
## PersonCollection::Contains method


确定集合中是否包含特定人员。

```cpp
bool Aspose::Words::Bibliography::PersonCollection::Contains(const System::SharedPtr<Aspose::Words::Bibliography::Person> &person)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 人物 | const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\& | 要在集合中定位的人员。 |

## 示例



展示如何使用人物集合。
```cpp
// 创建一个新的人物集合。
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// 向集合中添加新人物。
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// 如果存在，则从集合中移除人物。
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// 创建包含两个人物的集合。
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// 通过索引从集合中移除人物。
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// 从集合中移除所有人物。
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## 另见

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
