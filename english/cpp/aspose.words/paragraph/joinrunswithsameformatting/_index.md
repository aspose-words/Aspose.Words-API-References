---
title: Aspose::Words::Paragraph::JoinRunsWithSameFormatting method
linktitle: JoinRunsWithSameFormatting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph::JoinRunsWithSameFormatting method. Joins runs with the same formatting in the paragraph in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph::JoinRunsWithSameFormatting() method


Joins runs with the same formatting in the paragraph.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting()
```


### ReturnValue

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.

## Examples



Shows how to simplify paragraphs by merging superfluous runs. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert four runs of text into the paragraph.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");
builder->Write(u"Run 3. ");
builder->Write(u"Run 4. ");

// If we open this document in Microsoft Word, the paragraph will look like one seamless text body.
// However, it will consist of four separate runs with the same formatting. Fragmented paragraphs like this
// may occur when we manually edit parts of one paragraph many times in Microsoft Word.
System::SharedPtr<Aspose::Words::Paragraph> para = builder->get_CurrentParagraph();

ASSERT_EQ(4, para->get_Runs()->get_Count());

// Change the style of the last run to set it apart from the first three.
para->get_Runs()->idx_get(3)->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Emphasis);

// We can run the "JoinRunsWithSameFormatting" method to optimize the document's contents
// by merging similar runs into one, reducing their overall count.
// This method also returns the number of runs that this method merged.
// These two merges occurred to combine Runs #1, #2, and #3,
// while leaving out Run #4 because it has an incompatible style.
ASSERT_EQ(2, para->JoinRunsWithSameFormatting());

// The number of runs left will equal the original count
// minus the number of run merges that the "JoinRunsWithSameFormatting" method carried out.
ASSERT_EQ(2, para->get_Runs()->get_Count());
ASSERT_EQ(u"Run 1. Run 2. Run 3. ", para->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"Run 4. ", para->get_Runs()->idx_get(1)->get_Text());
```

## See Also

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) method


Joins runs with the same formatting in the paragraph.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr<Aspose::Words::JoinRunsOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| options | const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\& | Additional options |

### ReturnValue

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.

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

* Class [JoinRunsOptions](../../joinrunsoptions/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
