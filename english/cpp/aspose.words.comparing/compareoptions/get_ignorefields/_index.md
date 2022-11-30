---
title: get_IgnoreFields
second_title: Aspose.Words for C++ API Reference
description: Specifies whether to compare differences in fields. By default fields are not ignored.
type: docs
weight: 66
url: /cpp/aspose.words.comparing/compareoptions/get_ignorefields/
---
## CompareOptions::get_IgnoreFields method


Specifies whether to compare differences in fields. By default fields are not ignored.

```cpp
bool Aspose::Words::Comparing::CompareOptions::get_IgnoreFields() const
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

## See Also

* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words](../../../)
