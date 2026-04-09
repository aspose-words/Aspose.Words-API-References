---
title: Aspose::Words::JoinRunsOptions class
linktitle: JoinRunsOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::JoinRunsOptions class. Provides configuration flags for the join runs operation in C++.'
type: docs
weight: 38500
url: /cpp/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class


Provides configuration flags for the join runs operation.

```cpp
class JoinRunsOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_IgnoreInsignificant](./get_ignoreinsignificant/)() const | True indicates that the insignificant attributes of all runs will be ignored when joining runs with same formatting. |
| [get_IgnoreRedundant](./get_ignoreredundant/)() const | True indicates that the redundant attributes of all runs will be ignored when joining runs with same formatting. |
| [get_IgnoreSpacing](./get_ignorespacing/)() const | True indicates that the spacing attributes of all runs will be ignored when joining runs with same formatting. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsOptions](./joinrunsoptions/)() |  |
| [set_IgnoreInsignificant](./set_ignoreinsignificant/)(bool) | True indicates that the insignificant attributes of all runs will be ignored when joining runs with same formatting. |
| [set_IgnoreRedundant](./set_ignoreredundant/)(bool) | True indicates that the redundant attributes of all runs will be ignored when joining runs with same formatting. |
| [set_IgnoreSpacing](./set_ignorespacing/)(bool) | True indicates that the spacing attributes of all runs will be ignored when joining runs with same formatting. |
| static [Type](./type/)() |  |

## Examples



Shows how to join runs with the same formatting while ignoring redundant and insignificant attributes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Create runs with identical visible formatting but some internal differences.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Verify runs before join.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Configure options to ignore redundant and insignificant attributes during join.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Ignore redundant run properties that don't affect appearance.
options->set_IgnoreInsignificant(true);
// Ignore insignificant differences like whitespace-only runs.

// Join runs that have the same visible formatting using the extended options.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Verify that runs were successfully joined.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
