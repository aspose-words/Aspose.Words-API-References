---
title: Aspose::Words::Fields::FieldSeq class
linktitle: FieldSeq
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldSeq class. Implements the SEQ field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 91000
url: /cpp/aspose.words.fields/fieldseq/
---
## FieldSeq class


Implements the SEQ field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldSeq : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Gets a bookmark name that refers to an item elsewhere in the document rather than in the current location. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_InsertNextNumber](./get_insertnextnumber/)() | Gets or sets whether to insert the next sequence number for the specified item. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_ResetHeadingLevel](./get_resetheadinglevel/)() | Gets or sets an integer number representing a heading level to reset the sequence number to. Returns -1 if the number is absent. |
| [get_ResetNumber](./get_resetnumber/)() | Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_SequenceIdentifier](./get_sequenceidentifier/)() | Gets or sets the name assigned to the series of items that are to be numbered. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Sets a bookmark name that refers to an item elsewhere in the document rather than in the current location. |
| [set_InsertNextNumber](./set_insertnextnumber/)(bool) | Setter for [Aspose::Words::Fields::FieldSeq::get_InsertNextNumber](./get_insertnextnumber/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ResetHeadingLevel](./set_resetheadinglevel/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel](./get_resetheadinglevel/). |
| [set_ResetNumber](./set_resetnumber/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldSeq::get_ResetNumber](./get_resetnumber/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceIdentifier](./set_sequenceidentifier/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier](./get_sequenceidentifier/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to populate a TOC field with entries using SEQ fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A TOC field can create an entry in its table of contents for each SEQ field found in the document.
// Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
auto fieldToc = System::ExplicitCast<FieldToc>(builder->InsertField(FieldType::FieldTOC, true));

// SEQ fields display a count that increments at each SEQ field.
// These fields also maintain separate counts for each unique named sequence
// identified by the SEQ field's "SequenceIdentifier" property.
// Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
// Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
// SEQ fields from this prefix sequence will not create TOC entries.
// Every TOC entry created from a main sequence SEQ field will now also display the count that
// the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Each TOC entry will display the prefix sequence count immediately to the left
// of the page number that the main sequence SEQ field appears on.
// We can specify a custom separator that will appear between these two numbers.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(BreakType::PageBreak);

// There are two ways of using SEQ fields to populate this TOC.
// 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
// This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
// Since this field does not belong to the main sequence identified
// by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
auto fieldSeq = System::ExplicitCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
// This SEQ field will create an entry in the TOC.
// The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
// This entry will also display the count that the prefix sequence is currently at,
// separated from the page number by the value in the TOC's SeqenceSeparator property.
// The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
// and the separator is ">", so entry will display "1>2".
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
// The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
// so the TOC entry will display "2>3" at its page count.
builder->InsertBreak(BreakType::PageBreak);
fieldSeq = System::ExplicitCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.TOC.SEQ.docx");
```


Shows create numbering using SEQ fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// SEQ fields display a count that increments at each SEQ field.
// These fields also maintain separate counts for each unique named sequence
// identified by the SEQ field's "SequenceIdentifier" property.
// Insert a SEQ field that will display the current count value of "MySequence",
// after using the "ResetNumber" property to set it to 100.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Display the next number in this sequence with another SEQ field.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// Insert a level 1 heading.
builder->InsertBreak(BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// The above heading is a level 1 heading, so the count for this sequence is reset to 1.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Move to the next number of this sequence.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.SEQ.ResetNumbering.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
