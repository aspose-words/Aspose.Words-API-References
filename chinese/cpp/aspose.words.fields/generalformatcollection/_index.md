---
title: "Aspose::Words::Fields::GeneralFormatCollection 类"
linktitle: "GeneralFormatCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::GeneralFormatCollection 类。表示一个通用格式的类型化集合。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 114000
url: /zh/cpp/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class


表示通用格式的类型化集合。要了解更多信息，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class GeneralFormatCollection : public System::Collections::Generic::IEnumerable<Aspose::Words::Fields::GeneralFormat>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(Aspose::Words::Fields::GeneralFormat) | 向集合中添加通用格式。 |
| [get_Count](./get_count/)() | 获取集合中项目的总数。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 获取指定索引处的通用格式。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(Aspose::Words::Fields::GeneralFormat) | 从集合中移除所有指定通用格式的出现。 |
| [RemoveAt](./removeat/)(int32_t) | 在指定索引处移除一个通用格式的出现。 |
| static [Type](./type/)() |  |

## 示例



展示如何格式化字段结果。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用文档生成器插入一个字段，以显示未应用任何格式的结果。
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// 我们可以使用字段的属性为字段结果应用格式。
// 下面是我们可以应用于字段结果的三种格式类型。
// 1 - 数值格式：
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 - 日期/时间格式：
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 - 常规格式：
field = builder->InsertField(u"= 25 + 33");
format = field->get_Format();
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::Upper);
field->Update();

int32_t index = 0;
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<Aspose::Words::Fields::GeneralFormat>> generalFormatEnumerator = format->get_GeneralFormats()->GetEnumerator();
    while (generalFormatEnumerator->MoveNext())
    {
        std::cout << System::String::Format(u"General format index {0}: {1}", index++, generalFormatEnumerator->get_Current()) << std::endl;
    }
}

ASSERT_EQ(u"= 25 + 33 \\* roman \\* Upper", field->GetFieldCode());
ASSERT_EQ(u"LVIII", field->get_Result());
ASSERT_EQ(2, format->get_GeneralFormats()->get_Count());
ASSERT_EQ(Aspose::Words::Fields::GeneralFormat::LowercaseRoman, format->get_GeneralFormats()->idx_get(0));

// 我们可以移除格式，将字段结果恢复到原始形式。
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
