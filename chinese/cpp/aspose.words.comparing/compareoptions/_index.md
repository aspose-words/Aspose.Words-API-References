---
title: "Aspose::Words::Comparing::CompareOptions class"
linktitle: "CompareOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comparing::CompareOptions class。允许为文档比较操作选择其他选项。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.comparing/compareoptions/
---
## CompareOptions class


允许为文档比较操作选择其他选项。欲了解更多信息，请访问 [Compare Documents](https://docs.aspose.com/words/cpp/compare-documents/) 文档文章。

```cpp
class CompareOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [CompareOptions](./compareoptions/)() |  |
| [get_AdvancedOptions](./get_advancedoptions/)() const | 指定高级比较选项，可能有助于生成更精确的比较输出。 |
| [get_CompareMoves](./get_comparemoves/)() const | 指定是否比较两个文档之间的差异。 |
| [get_Granularity](./get_granularity/)() const | 指定更改是按字符还是按单词进行跟踪。 |
| [get_IgnoreCaseChanges](./get_ignorecasechanges/)() const | True 表示文档比较不区分大小写。 |
| [get_IgnoreComments](./get_ignorecomments/)() const | 指定是否比较批注中的差异。 |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() | 指定是否忽略 DrawingML 唯一标识的差异。 |
| [get_IgnoreFields](./get_ignorefields/)() const | 指定是否比较字段中的差异。 |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | 指定是否比较脚注和尾注中的差异。 |
| [get_IgnoreFormatting](./get_ignoreformatting/)() const | True 表示格式被忽略。 |
| [get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/)() const | True 表示页眉和页脚内容被忽略。 |
| [get_IgnoreTables](./get_ignoretables/)() const | 指定是否比较表格中包含的数据差异。 |
| [get_IgnoreTextboxes](./get_ignoretextboxes/)() const | 指定是否比较文本框中包含的数据差异。 |
| [get_Target](./get_target/)() const | 指定在比较期间应使用哪个文档作为目标。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CompareMoves](./set_comparemoves/)(bool) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_CompareMoves](./get_comparemoves/)。 |
| [set_Granularity](./set_granularity/)(Aspose::Words::Comparing::Granularity) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_Granularity](./get_granularity/)。 |
| [set_IgnoreCaseChanges](./set_ignorecasechanges/)(bool) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_IgnoreCaseChanges](./get_ignorecasechanges/)。 |
| [set_IgnoreComments](./set_ignorecomments/)(bool) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_IgnoreComments](./get_ignorecomments/)。 |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)。 |
| [set_IgnoreFields](./set_ignorefields/)(bool) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_IgnoreFields](./get_ignorefields/)。 |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_IgnoreFootnotes](./get_ignorefootnotes/)。 |
| [set_IgnoreFormatting](./set_ignoreformatting/)(bool) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_IgnoreFormatting](./get_ignoreformatting/)。 |
| [set_IgnoreHeadersAndFooters](./set_ignoreheadersandfooters/)(bool) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/)。 |
| [set_IgnoreTables](./set_ignoretables/)(bool) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_IgnoreTables](./get_ignoretables/)。 |
| [set_IgnoreTextboxes](./set_ignoretextboxes/)(bool) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_IgnoreTextboxes](./get_ignoretextboxes/)。 |
| [set_Target](./set_target/)(Aspose::Words::Comparing::ComparisonTargetType) | 用于设置 [Aspose::Words::Comparing::CompareOptions::get_Target](./get_target/)。 |
| static [Type](./type/)() |  |

## 示例



展示在进行比较时如何过滤特定类型的文档元素。
```cpp
// 创建原始文档并填充各种元素。
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);

// 带有尾注的段落文本：
builder->Writeln(u"Hello world! This is the first paragraph.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Original endnote text.");

// 表格：
builder->StartTable();
builder->InsertCell();
builder->Write(u"Original cell 1 text");
builder->InsertCell();
builder->Write(u"Original cell 2 text");
builder->EndTable();

// 文本框：
System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 20);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"Original textbox contents");

// DATE 字段：
builder->MoveTo(docOriginal->get_FirstSection()->get_Body()->AppendParagraph(u""));
builder->InsertField(u" DATE ");

// 批注：
auto newComment = System::MakeObject<Aspose::Words::Comment>(docOriginal, u"John Doe", u"J.D.", System::DateTime::get_Now());
newComment->SetText(u"Original comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(newComment);

// 页眉：
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Original header contents.");

// 创建文档的克隆并对克隆文档的每个元素进行快速编辑。
auto docEdited = System::ExplicitCast<Aspose::Words::Document>(System::ExplicitCast<Aspose::Words::Node>(docOriginal)->Clone(true));
System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = docEdited->get_FirstSection()->get_Body()->get_FirstParagraph();

firstParagraph->get_Runs()->idx_get(0)->set_Text(u"hello world! this is the first paragraph, after editing.");
firstParagraph->get_ParagraphFormat()->set_Style(docEdited->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1));
(System::ExplicitCast<Aspose::Words::Notes::Footnote>(docEdited->GetChild(Aspose::Words::NodeType::Footnote, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(1)->set_Text(u"Edited endnote text.");
(System::ExplicitCast<Aspose::Words::Tables::Table>(docEdited->GetChild(Aspose::Words::NodeType::Table, 0, true)))->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited Cell 2 contents");
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(docEdited->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited textbox contents");
(System::ExplicitCast<Aspose::Words::Fields::FieldDate>(docEdited->get_Range()->get_Fields()->idx_get(0)))->set_UseLunarCalendar(true);
(System::ExplicitCast<Aspose::Words::Comment>(docEdited->GetChild(Aspose::Words::NodeType::Comment, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited comment.");
docEdited->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited header contents.");

// 比较文档会为已编辑文档中的每一次编辑创建一个修订。
// 一个 CompareOptions 对象具有一系列可以抑制修订的标志。
// 对每种相应类型的元素，有效地忽略它们的更改。
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_CompareMoves(false);
compareOptions->set_IgnoreFormatting(false);
compareOptions->set_IgnoreCaseChanges(false);
compareOptions->set_IgnoreComments(false);
compareOptions->set_IgnoreTables(false);
compareOptions->set_IgnoreFields(false);
compareOptions->set_IgnoreFootnotes(false);
compareOptions->set_IgnoreTextboxes(false);
compareOptions->set_IgnoreHeadersAndFooters(false);
compareOptions->set_Target(Aspose::Words::Comparing::ComparisonTargetType::New);

docOriginal->Compare(docEdited, u"John Doe", System::DateTime::get_Now(), compareOptions);
docOriginal->Save(get_ArtifactsDir() + u"Revision.CompareOptions.docx");
```

## 另见

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
