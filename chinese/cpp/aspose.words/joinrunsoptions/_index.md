---
title: "Aspose::Words::JoinRunsOptions 类"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::JoinRunsOptions 类。提供用于 C++ 中连接运行操作的配置标志。"
type: docs
weight: 38500
url: /zh/cpp/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class


提供用于连接运行操作的配置标志。

```cpp
class JoinRunsOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_IgnoreInsignificant](./get_ignoreinsignificant/)() const | True 表示在合并具有相同格式的运行时，所有运行的微不足道属性将被忽略。 |
| [get_IgnoreRedundant](./get_ignoreredundant/)() const | True 表示在合并具有相同格式的运行时，所有运行的冗余属性将被忽略。 |
| [get_IgnoreSpacing](./get_ignorespacing/)() const | True 表示在合并具有相同格式的运行时，所有运行的间距属性将被忽略。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsOptions](./joinrunsoptions/)() |  |
| [set_IgnoreInsignificant](./set_ignoreinsignificant/)(bool) | True 表示在合并具有相同格式的运行时，所有运行的微不足道属性将被忽略。 |
| [set_IgnoreRedundant](./set_ignoreredundant/)(bool) | True 表示在合并具有相同格式的运行时，所有运行的冗余属性将被忽略。 |
| [set_IgnoreSpacing](./set_ignorespacing/)(bool) | True 表示在合并具有相同格式的运行时，所有运行的间距属性将被忽略。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
