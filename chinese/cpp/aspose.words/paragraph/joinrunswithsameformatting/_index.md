---
title: "Aspose::Words::Paragraph::JoinRunsWithSameFormatting 方法"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::JoinRunsWithSameFormatting 方法。将段落中具有相同格式的运行合并（C++）。"
type: docs
weight: 31000
url: /zh/cpp/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph::JoinRunsWithSameFormatting() method


合并段落中具有相同格式的运行。

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting()
```


### ReturnValue

已执行的合并次数。当 **N** 个相邻的运行被合并时，它们计为 **N - 1** 次合并。

## 示例



展示如何通过合并多余的运行来简化段落。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在段落中插入四个文本运行。
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");
builder->Write(u"Run 3. ");
builder->Write(u"Run 4. ");

// 如果在 Microsoft Word 中打开此文档，段落将呈现为一个连续的文本主体。
// 然而，它实际上由四个具有相同格式的独立运行组成。这样的碎片化段落
// 可能在我们多次手动编辑同一段落的部分时出现（在 Microsoft Word 中）。
System::SharedPtr<Aspose::Words::Paragraph> para = builder->get_CurrentParagraph();

ASSERT_EQ(4, para->get_Runs()->get_Count());

// 更改最后一个运行的样式，使其与前三个区别开来。
para->get_Runs()->idx_get(3)->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Emphasis);

// 我们可以运行 "JoinRunsWithSameFormatting" 方法来优化文档的内容
// 通过将相似的运行合并为一个，减少它们的总数量。
// 此方法还会返回该方法合并的运行数量。
// 这两次合并用于将运行 #1、#2 和 #3 合并，
// 而排除运行 #4，因为它的样式不兼容。
ASSERT_EQ(2, para->JoinRunsWithSameFormatting());

// 剩余运行的数量将等于原始计数
// 减去 "JoinRunsWithSameFormatting" 方法执行的运行合并次数。
ASSERT_EQ(2, para->get_Runs()->get_Count());
ASSERT_EQ(u"Run 1. Run 2. Run 3. ", para->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"Run 4. ", para->get_Runs()->idx_get(1)->get_Text());
```

## 另见

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) method


合并段落中具有相同格式的运行。

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr<Aspose::Words::JoinRunsOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| options | const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\& | 其他选项 |

### ReturnValue

已执行的合并次数。当 **N** 个相邻的运行被合并时，它们计为 **N - 1** 次合并。

## 示例



展示如何在忽略冗余和微不足道属性的情况下，合并具有相同格式的运行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建具有相同可见格式但内部有一些差异的运行。
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// 在合并前验证运行。
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// 配置选项以在合并期间忽略冗余和微不足道的属性。
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// 忽略不会影响外观的冗余运行属性。
options->set_IgnoreInsignificant(true);
// 忽略诸如仅包含空白的运行等微不足道的差异。

// 使用扩展选项合并具有相同可见格式的运行。
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// 验证运行已成功合并。
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## 另见

* Class [JoinRunsOptions](../../joinrunsoptions/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
