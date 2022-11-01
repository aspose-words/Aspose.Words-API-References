---
title: Compare
second_title: Aspose.Words for C++ API Reference
description: Compares this document with another document producing changes as number of edit and format revisions Revision.
type: docs
weight: 79
url: /cpp/aspose.words/document/compare/
---
## Document.Compare(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) method


Compares this document with another document producing changes as number of edit and format revisions [Revision](../../revision/).

```cpp
void Aspose::Words::Document::Compare(const System::SharedPtr<Aspose::Words::Document> &document, const System::String &author, System::DateTime dateTime)
```


| Parameter | Type | Description |
| --- | --- | --- |
| document | const System::SharedPtr\<Aspose::Words::Document\>\& | [Document](../) to compare. |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |

The following document nodes are not compared at the moment:

* [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Item3




Documents must not have revisions before comparison.
## Examples




Shows how to compare documents. 
```cpp
auto docOriginal = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = MakeObject<Document>();
builder = MakeObject<DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// Comparing documents with revisions will throw an exception.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// After the comparison, the original document will gain a new revision
// for every element that is different in the edited document.
for (const auto& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType())
              << std::endl;
    std::cout << "\tChanged text: \"" << r->get_ParentNode()->GetText() << "\"" << std::endl;
}

// Accepting these revisions will transform the original document into the edited document.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## Document.Compare(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compares this document with another document producing changes as a number of edit and format revisions [Revision](../../revision/). Allows to specify comparison options using [CompareOptions](../../../aspose.words.comparing/compareoptions/).

```cpp
void Aspose::Words::Document::Compare(const System::SharedPtr<Aspose::Words::Document> &document, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &options)
```


## Examples




Shows how to filter specific types of document elements when making a comparison. 
```cpp
// Create the original document and populate it with various kinds of elements.
auto docOriginal = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(docOriginal);

// Paragraph text referenced with an endnote:
builder->Writeln(u"Hello world! This is the first paragraph.");
builder->InsertFootnote(FootnoteType::Endnote, u"Original endnote text.");

// Table:
builder->StartTable();
builder->InsertCell();
builder->Write(u"Original cell 1 text");
builder->InsertCell();
builder->Write(u"Original cell 2 text");
builder->EndTable();

// Textbox:
SharedPtr<Shape> textBox = builder->InsertShape(ShapeType::TextBox, 150, 20);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"Original textbox contents");

// DATE field:
builder->MoveTo(docOriginal->get_FirstSection()->get_Body()->AppendParagraph(u""));
builder->InsertField(u" DATE ");

// Comment:
auto newComment = MakeObject<Comment>(docOriginal, u"John Doe", u"J.D.", System::DateTime::get_Now());
newComment->SetText(u"Original comment.");
builder->get_CurrentParagraph()->AppendChild(newComment);

// Header:
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Original header contents.");

// Create a clone of our document and perform a quick edit on each of the cloned document's elements.
auto docEdited = System::DynamicCast<Document>(docOriginal->Clone(true));
SharedPtr<Paragraph> firstParagraph = docEdited->get_FirstSection()->get_Body()->get_FirstParagraph();

firstParagraph->get_Runs()->idx_get(0)->set_Text(u"hello world! this is the first paragraph, after editing.");
firstParagraph->get_ParagraphFormat()->set_Style(docEdited->get_Styles()->idx_get(StyleIdentifier::Heading1));
(System::DynamicCast<Footnote>(docEdited->GetChild(NodeType::Footnote, 0, true)))
    ->get_FirstParagraph()
    ->get_Runs()
    ->idx_get(1)
    ->set_Text(u"Edited endnote text.");
(System::DynamicCast<Table>(docEdited->GetChild(NodeType::Table, 0, true)))
    ->get_FirstRow()
    ->get_Cells()
    ->idx_get(1)
    ->get_FirstParagraph()
    ->get_Runs()
    ->idx_get(0)
    ->set_Text(u"Edited Cell 2 contents");
(System::DynamicCast<Shape>(docEdited->GetChild(NodeType::Shape, 0, true)))
    ->get_FirstParagraph()
    ->get_Runs()
    ->idx_get(0)
    ->set_Text(u"Edited textbox contents");
(System::DynamicCast<FieldDate>(docEdited->get_Range()->get_Fields()->idx_get(0)))->set_UseLunarCalendar(true);
(System::DynamicCast<Comment>(docEdited->GetChild(NodeType::Comment, 0, true)))
    ->get_FirstParagraph()
    ->get_Runs()
    ->idx_get(0)
    ->set_Text(u"Edited comment.");
docEdited->get_FirstSection()
    ->get_HeadersFooters()
    ->idx_get(HeaderFooterType::HeaderPrimary)
    ->get_FirstParagraph()
    ->get_Runs()
    ->idx_get(0)
    ->set_Text(u"Edited header contents.");

// Comparing documents creates a revision for every edit in the edited document.
// A CompareOptions object has a series of flags that can suppress revisions
// on each respective type of element, effectively ignoring their change.
auto compareOptions = MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_IgnoreFormatting(false);
compareOptions->set_IgnoreCaseChanges(false);
compareOptions->set_IgnoreComments(false);
compareOptions->set_IgnoreTables(false);
compareOptions->set_IgnoreFields(false);
compareOptions->set_IgnoreFootnotes(false);
compareOptions->set_IgnoreTextboxes(false);
compareOptions->set_IgnoreHeadersAndFooters(false);
compareOptions->set_Target(ComparisonTargetType::New);

docOriginal->Compare(docEdited, u"John Doe", System::DateTime::get_Now(), compareOptions);
docOriginal->Save(ArtifactsDir + u"Document.CompareOptions.docx");
```

