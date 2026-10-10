---
title: "Aspose::Words::Fields::GeneralFormat 枚举"
linktitle: "GeneralFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::GeneralFormat 枚举。指定应用于数值、文本或任何字段结果的通用格式。字段在 C++ 中可能具有组合的通用格式。"
type: docs
weight: 132000
url: /zh/cpp/aspose.words.fields/generalformat/
---
## GeneralFormat enum


指定应用于数值、文本或任何字段结果的一般格式。字段可以具有多个一般格式的组合。

```cpp
enum class GeneralFormat
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 用于指定缺失的通用格式。 |
| Aiueo | 1 | 数值格式化。使用传统的 a-i-u-e-o 顺序的平假名字符对数值结果进行格式化。 |
| UppercaseAlphabetic | 2 | 数值格式化。将数值结果格式化为一个或多个大写拉丁字母字符。 |
| LowercaseAlphabetic | 3 | 数值格式化。将数值结果格式化为一个或多个小写拉丁字母字符。 |
| Arabic | 4 | 数值格式化。使用阿拉伯基数数字格式化数值结果。 |
| ArabicAbjad | 5 | 数值格式化。使用递增的阿布贾数字格式化数值结果。 |
| ArabicAlpha | 6 | 数值格式化。使用阿拉伯字母表中的字符格式化数值结果。 |
| ArabicDash | 7 | 数值格式化。使用阿拉伯基数数字格式化数值结果，前缀为 "- "，后缀为 " -"。 |
| BahtText | 8 | 数值格式化。使用泰国计数系统格式化数值结果。 |
| CardText | 9 | 数值格式化。基数文本（一，二，三，...）。 |
| ChineseNum1 | 10 | 数值格式化。使用相应计数系统中的递增数字格式化数值结果。 |
| ChineseNum2 | 11 | 数值格式化。使用相应法律格式中的顺序数字格式化数值结果。 |
| ChineseNum3 | 12 | 数值格式化。使用相应千位计数系统中的顺序数字格式化数值结果。 |
| Chosung | 13 | 数值格式化。使用韩文初声（Chosung）格式中的顺序数字格式化数值结果。 |
| CircleNum | 14 | 数值格式化。使用圆圈包围的十进制编号格式化数值结果，采用 1–20 范围内的封闭字母数字字符。 |
| DBChar | 15 | 数值格式化。使用双字节阿拉伯数字格式化数值结果。 |
| DBNum1 | 16 | 数值格式化。使用顺序数字表意文字格式化数值结果，使用适当的字符。 |
| DBNum2 | 17 | 数值格式化。使用来自适当计数系统的顺序数字格式化数值结果。 |
| DBNum3 | 18 | 数值格式化。使用来自适当法律计数系统的顺序数字格式化数值结果。 |
| DBNum4 | 19 | 数值格式化。使用来自适当数字计数系统的顺序数字格式化数值结果。 |
| DollarText | 20 | 数值格式化。美元文字（One, Two, Three, ... + AND 55/100）。 |
| Ganada | 21 | 数值格式化。使用来自 Korean Ganada 格式的顺序数字格式化数值结果。 |
| GB1 | 22 | 数值格式化。使用带句点的十进制编号格式化数值结果，使用封闭的字母数字字形字符。 |
| GB2 | 23 | 数值格式化。使用括号内的十进制编号格式化数值结果，使用封闭的字母数字字形字符。 |
| GB3 | 24 | 数值格式化。使用圆圈内的十进制编号格式化数值结果，使用封闭的字母数字字形字符。 |
| GB4 | 25 | 数值格式化。使用圆圈内的十进制编号格式化数值结果，使用封闭的字母数字字形字符。 |
| Hebrew1 | 26 | 数值格式化。使用希伯来数字格式化数值结果。 |
| 希伯来语2 | 27 | 数值格式化。使用希伯来字母表格式化数值结果。 |
| 十六进制 | 28 | 数值格式化。使用大写十六进制数字格式化数值结果。 |
| 印地语阿拉伯语 | 29 | 数值格式化。使用印地语数字格式化数值结果。 |
| HindiCardText | 30 | 数值格式化。使用来自印地语计数系统的顺序数字格式化数值结果。 |
| 印地语字母1 | 31 | 数值格式化。使用印地语元音格式化数值结果。 |
| 印地语字母2 | 32 | 数值格式化。使用印地语辅音格式化数值结果。 |
| Iroha | 33 | 数值格式化。使用日文 iroha 格式化数值结果。 |
| KanjiNum1 | 34 | 数值格式化。使用适当计数系统的日式风格格式化数值结果。 |
| KanjiNum2 | 35 | 数字格式化。使用适当的计数系统格式化数值结果。 |
| KanjiNum3 | 36 | 数字格式化。使用适当的计数系统格式化数值结果。 |
| 序数 | 37 | 数字格式化。序数（第1，第2，第3，...）。 |
| OrdText | 38 | 数字格式化。序数文本（第一，第二，第三，...）。 |
| UppercaseRoman | 39 | 数字格式化。大写罗马数字（I，II，III，...）。 |
| LowercaseRoman | 40 | 数字格式化。小写罗马数字（i，ii，iii，...）。 |
| SBChar | 41 | 数字格式化。使用单字节阿拉伯数字格式化数值结果。 |
| 泰语阿拉伯语 | 42 | 数字格式化。使用泰国数字格式化数值结果。 |
| ThaiCardText | 43 | 数字格式化。使用泰国计数系统的顺序数字格式化数值结果。 |
| 泰文字母 | 44 | 数字格式化。使用泰文字母格式化数值结果。 |
| VietCardText | 45 | 数字格式化。使用越南数字格式化数值结果。 |
| Zodiac1 | 46 | 数字格式化。使用顺序的传统数字表意文字格式化数值结果。 |
| Zodiac2 | 47 | 数字格式化。使用顺序的生肖表意文字格式化数值结果。 |
| Zodiac3 | 48 | 数字格式化。使用顺序的传统生肖表意文字格式化数值结果。 |
| Caps | 49 | 文本格式化。将每个单词的首字母大写。 |
| FirstCap | 50 | 文本格式化。将第一个单词的首字母大写。 |
| Lower | 51 | 文本格式化。所有字母均为小写。 |
| 大写 | 52 | 文本格式化。所有字母均为大写。 |
| CharFormat | 53 | [Field](../field/) 结果格式化。CHARFORMAT 指令。 |
| MergeFormat | 54 | [Field](../field/) 结果格式化。MERGEFORMAT 指令。 |
| MergeFormatInet | 55 | [Field](../field/) 结果格式化。MERGEFORMATINET 指令。 |


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
