---
title: "Aspose::Words::Range::Replace 方法"
linktitle: "Replace"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Range::Replace 方法。将正则表达式指定的字符模式的所有出现替换为另一个字符串（使用 C++）。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/range/replace/
---
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


将正则表达式指定的字符模式的所有出现替换为另一个字符串。

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


替换正则表达式捕获的整个匹配项。

该方法能够处理模式和替换字符串中的换行。

如果需要处理换行，请使用特殊的元字符：

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## 示例



展示如何将正则表达式模式的所有出现替换为其他文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"I decided to get the curtains in gray, ideal for the grey-accented room.");

doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"gr(a|e)y"), u"lavender");

ASSERT_EQ(u"I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc->GetText().Trim());
```

## 另见

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


将正则表达式指定的字符模式的所有出现替换为另一个字符串。

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 模式 | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | 用于查找匹配项的正则表达式模式。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

### ReturnValue

已完成的替换次数。
## 备注


替换正则表达式捕获的整个匹配项。

该方法能够处理模式和替换字符串中的换行。

如果需要处理换行，请使用特殊的元字符：

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## 另见

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&) method


将指定字符字符串模式的所有出现替换为替换字符串。

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |

### ReturnValue

已完成的替换次数。
## 备注


该模式将不被视为正则表达式。如果需要正则表达式，请使用 [Replace()](../)。

使用不区分大小写的比较。

该方法能够处理模式和替换字符串中的换行。

如果需要处理换行，请使用特殊的元字符：

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## 示例



展示如何在文档内容上执行查找替换文本操作。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Greetings, _FullName_!");

// 对文档内容执行查找替换操作，并验证实际发生的替换次数。
int32_t replacementCount = doc->get_Range()->Replace(u"_FullName_", u"John Doe");

ASSERT_EQ(1, replacementCount);
ASSERT_EQ(u"Greetings, John Doe!", doc->GetText().Trim());
```


展示如何为在查找替换操作中找到匹配的段落添加格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Set the "Alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
// 其中包含查找替换操作找到的匹配项。
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// 将每个紧跟段落换行符之前的句号替换为感叹号。
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## 另见

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


将指定字符字符串模式的所有出现替换为替换字符串。

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 模式 | const System::String\& | 待替换的字符串。 |
| 替换文本 | const System::String\& | 用于替换模式所有出现的字符串。 |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) 对象，用于指定其他选项。 |

### ReturnValue

已完成的替换次数。
## 备注


该模式将不被视为正则表达式。如果需要正则表达式，请使用 [Replace()](../)。

该方法能够处理模式和替换字符串中的换行。

如果需要处理换行，请使用特殊的元字符：

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## 示例



展示如何替换文档页脚中的文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```


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


展示如何在表格和单元格中替换所有文本实例。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Carrots");
builder->InsertCell();
builder->Write(u"50");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Potatoes");
builder->InsertCell();
builder->Write(u"50");
builder->EndTable();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(true);
options->set_FindWholeWordsOnly(true);

// 对整个表格执行查找替换操作。
table->get_Range()->Replace(u"Carrots", u"Eggs", options);

// 对表格最后一行的最后一个单元格执行查找替换操作。
table->get_LastRow()->get_LastCell()->get_Range()->Replace(u"50", u"20", options);

ASSERT_EQ(System::String(u"Eggs\a50\a\a") + u"Potatoes\a20\a\a", table->GetText().Trim());
```

## 另见

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
