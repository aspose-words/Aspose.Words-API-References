---
title: "Aspose::Words::NumberStyle enum"
linktitle: "NumberStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NumberStyle enum. 指定 C++ 中列表、脚注和尾注、页码的数字样式。"
type: docs
weight: 103000
url: /zh/cpp/aspose.words/numberstyle/
---
## NumberStyle enum


指定列表、脚注和尾注、页码的数字样式。

```cpp
enum class NumberStyle
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Arabic | 0 | Arabic 编号 (1, 2, 3, ...) |
| UppercaseRoman | 1 | 大写罗马数字 (I, II, III, ...) |
| LowercaseRoman | 2 | 小写罗马数字 (i, ii, iii, ...) |
| 大写字母 | 3 | 大写字母 (A, B, C, ...) |
| 小写字母 | 4 | 小写字母 (a, b, c, ...) |
| 序数 | 5 | 序数 (1st, 2nd, 3rd, ...) |
| 数字 | 6 | 编号 (One, Two, Three, ...) |
| 序数文本 | 7 | 序数（文本） (First, Second, Third, ...) |
| 十六进制 | 8 | 十六进制: 8, 9, A, B, C, D, E, F, 10, 11, 12. |
| ChicagoManual | 9 | 《芝加哥手册》[Style](../style/): *, †, † |
| 汉字 | 10 | 表意文字-数字。 |
| 汉字数字 | 11 | 日语计数。 |
| AiueoHalfWidth | 12 | Aiueo. |
| IrohaHalfWidth | 13 | Iroha. |
| ArabicFullWidth | 14 | 全宽阿拉伯数字：1, 2, 3, 4. |
| ArabicHalfWidth | 15 | 半宽阿拉伯数字：1, 2, 3, 4. |
| KanjiTraditional | 16 | 日文法律。 |
| KanjiTraditional2 | 17 | 日文数字万。 |
| NumberInCircle | 18 | 封闭圆圈。 |
| DecimalFullWidth | 19 | 十进制全宽：1, 2, 3, 4. |
| Aiueo | 20 | Aiueo 全宽。 |
| Iroha | 21 | Iroha 全角。 |
| LeadingZero | 22 | 前导零 (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | 23 | Bullet（检查文本中的字符代码） |
| Ganada | 24 | 韩文 Ganada。 |
| Chosung | 25 | 韩文 Chosung。 |
| GB1 | 26 | 封闭句点。 |
| GB2 | 27 | 封闭括号。 |
| GB3 | 28 | 封闭圆形中文。 |
| GB4 | 29 | 象形文字封闭圆。 |
| Zodiac1 | 30 | 象形文字传统。 |
| Zodiac2 | 31 | 象形文字生肖。 |
| Zodiac3 | 32 | 象形文字生肖传统。 |
| TradChinNum1 | 33 | 台湾计数。 |
| TradChinNum2 | 34 | 象形文字法律传统。 |
| TradChinNum3 | 35 | 台湾计数千。 |
| TradChinNum4 | 36 | 台湾数字。 |
| SimpChinNum1 | 37 | 中文计数。 |
| SimpChinNum2 | 38 | 简体中文法律。 |
| SimpChinNum3 | 39 | 中文千位计数。 |
| SimpChinNum4 | 40 | 中文（未实现） |
| HanjaRead | 41 | 韩文数字。 |
| HanjaReadDigit | 42 | 韩文计数。 |
| Hangul | 43 | 韩国法律。 |
| Hanja | 44 | 韩国数字2。 |
| Hebrew1 | 45 | Hebrew-1. |
| 阿拉伯语1 | 46 | 阿拉伯字母 alpha。 |
| 希伯来语2 | 47 | 希伯来语-2。 |
| 阿拉伯语2 | 48 | 阿拉伯字母表。 |
| 印地语字母1 | 49 | 印地语元音。 |
| 印地语字母2 | 50 | 印地语辅音。 |
| 印地语阿拉伯语 | 51 | 印地语数字。 |
| 印地语基数文本 | 52 | 印地语描述性（基数） |
| 泰文字母 | 53 | 泰文字母。 |
| 泰语阿拉伯语 | 54 | 泰文数字。 |
| ThaiCardinalText | 55 | 泰文描述（基数） |
| VietCardinalText | 56 | 越南文描述（基数） |
| NumberInDash | 57 | 页码格式：- 1 -，- 2 -，- 3 -，- 4 -。 |
| LowercaseRussian | 58 | 小写俄文字母表。 |
| UppercaseRussian | 59 | 大写俄文字母表。 |
| None | 255 | 无项目符号或编号。 |
| 自定义 | 65280 | 自定义数字格式。仅在 DOCX 格式中受支持。 |


## 示例



展示如何在使用 [DocumentBuilder](../documentbuilder/) 时对段落应用自定义列表格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
// 我们可以通过增加缩进级别来创建嵌套列表。
// 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
// 我们在列表开始和结束之间添加的每个段落都会成为列表中的一项。
// 从 Microsoft Word 模板创建列表，并自定义其前两个列表级别。
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// 此 NumberFormat 值将生成星形项目符号列表符号。
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// 创建段落并将我们自定义列表格式的两个级别应用于这些段落。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
