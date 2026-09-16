---
title: "Aspose::Words::Replacing::FindReplaceOptions class"
linktitle: "FindReplaceOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions class. 指定查找/替换操作的选项。欲了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


指定查找/替换操作的选项。欲了解更多，请访问[查找和替换](https://docs.aspose.com/words/cpp/find-and-replace/)文档文章。

```cpp
class FindReplaceOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() | 使用默认设置初始化 [FindReplaceOptions](./) 类的新实例。 |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) | 使用指定的方向初始化 [FindReplaceOptions](./) 类的新实例。 |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | 使用指定的替换回调初始化 [FindReplaceOptions](./) 类的新实例。 |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | 使用指定的方向和替换回调初始化 [FindReplaceOptions](./) 类的新实例。 |
| [get_ApplyFont](./get_applyfont/)() const | 文本格式化应用于新内容。 |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | [Paragraph](../../aspose.words/paragraph/) 格式已应用于新内容。 |
| [get_Direction](./get_direction/)() const | 选择替换的方向。默认值是 [Forward](../findreplacedirection/)。 |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True 表示 oldValue 必须是一个独立的单词。 |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | 获取或设置一个布尔值，指示是否忽略删除修订中的文本。默认值为 **false**。 |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | 获取或设置一个布尔值，指示是否忽略字段代码中的文本。默认值为 **false**。 |
| [get_IgnoreFields](./get_ignorefields/)() const | 获取或设置一个布尔值，指示是否忽略字段中的文本。默认值为 **false**。 |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | 获取或设置一个布尔值，指示是否忽略脚注。默认值为 **false**。 |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | 获取或设置一个布尔值，指示是否忽略插入修订中的文本。默认值为 **false**。 |
| [get_IgnoreOfficeMath](./get_ignoreofficemath/)() const | 获取或设置一个布尔值，指示是否忽略 OfficeMath/> 中的文本。默认值为 **true**。 |
| [get_IgnoreShapes](./get_ignoreshapes/)() const | 获取或设置一个布尔值，指示是否忽略文本中的形状。默认值为 **false**。 |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | 获取或设置一个布尔值，指示是否忽略 [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) 的内容。默认值为 **false**。 |
| [get_LegacyMode](./get_legacymode/)() const | 获取或设置一个布尔值，指示使用旧的查找/替换算法。 |
| [get_MatchCase](./get_matchcase/)() const | True 表示区分大小写比较，false 表示不区分大小写比较。 |
| [get_ReplacementFormat](./get_replacementformat/)() const | 指定替换的格式。默认是 [Text](../replacementformat/)。 |
| [get_ReplacingCallback](./get_replacingcallback/)() const | 在每次替换发生之前调用的用户定义方法。 |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | 获取或设置一个布尔值，指示在没有下一个同级段落时是否允许替换段落换行符。默认值为 **false**。 |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | True 表示在考虑文本框的情况下，文本搜索按从上到下的顺序进行。默认值为 **false**。 |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | 获取或设置一个布尔值，指示是否在替换模式中识别并使用替代项。默认值为 **false**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | 选择替换的方向。默认值是 [Forward](../findreplacedirection/)。 |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | 用于设置 [Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly](./get_findwholewordsonly/) 的 setter。 |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | 用于设置 [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted](./get_ignoredeleted/) 的 setter。 |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | 用于设置 [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes](./get_ignorefieldcodes/) 的 setter。 |
| [set_IgnoreFields](./set_ignorefields/)(bool) | 用于设置 [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields](./get_ignorefields/) 的 setter。 |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | 用于设置 [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes](./get_ignorefootnotes/) 的 setter。 |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | 用于设置 [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted](./get_ignoreinserted/) 的 setter。 |
| [set_IgnoreOfficeMath](./set_ignoreofficemath/)(bool) | 用于设置 [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath](./get_ignoreofficemath/) 的 setter。 |
| [set_IgnoreShapes](./set_ignoreshapes/)(bool) | 用于 [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes](./get_ignoreshapes/) 的设置器。 |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | 用于 [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/) 的设置器。 |
| [set_LegacyMode](./set_legacymode/)(bool) | 用于 [Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode](./get_legacymode/) 的设置器。 |
| [set_MatchCase](./set_matchcase/)(bool) | 用于 [Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase](./get_matchcase/) 的设置器。 |
| [set_ReplacementFormat](./set_replacementformat/)(Aspose::Words::Replacing::ReplacementFormat) | 指定替换的格式。默认是 [Text](../replacementformat/)。 |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | 在每次替换发生之前调用的用户定义方法。 |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | 用于 [Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/) 的设置器。 |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | True 表示在考虑文本框的情况下，文本搜索按从上到下的顺序进行。默认值为 **false**。 |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | 用于 [Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions](./get_usesubstitutions/) 的设置器。 |
| static [Type](./type/)() |  |

## 示例



展示如何在执行查找替换操作时切换大小写敏感性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// 将 "MatchCase" 标志设置为 "true"，以在查找要替换的字符串时启用大小写敏感。
// 将 "MatchCase" 标志设置为 "false"，以在搜索要替换的文本时忽略字符大小写。
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


展示如何切换仅针对独立单词的查找替换操作。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// 将 "FindWholeWordsOnly" 标志设置为 "true"，如果找到的文本不是其他单词的一部分，则进行替换。
// 将 "FindWholeWordsOnly" 标志设置为 "false"，无论其周围环境如何，都替换所有文本。
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## 另见

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
