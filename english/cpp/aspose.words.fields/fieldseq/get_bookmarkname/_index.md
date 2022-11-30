---
title: get_BookmarkName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location.
type: docs
weight: 1
url: /cpp/aspose.words.fields/fieldseq/get_bookmarkname/
---
## FieldSeq::get_BookmarkName method


Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_BookmarkName()
```


## Examples



Shows how to combine table of contents and sequence fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A TOC field can create an entry in its table of contents for each SEQ field found in the document.
// Each entry contains the paragraph that contains the SEQ field,
// and the number of the page that the field appears on.
auto fieldToc = System::DynamicCast<FieldToc>(builder->InsertField(FieldType::FieldTOC, true));

// Configure this TOC field to have a SequenceIdentifier property with a value of "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Configure this TOC field to only pick up SEQ fields that are within the bounds of a bookmark
// named "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// SEQ fields display a count that increments at each SEQ field.
// These fields also maintain separate counts for each unique named sequence
// identified by the SEQ field's "SequenceIdentifier" property.
// Insert a SEQ field that has a sequence identifier that matches the TOC's
// TableOfFiguresLabel property. This field will not create an entry in the TOC since it is outside
// the bookmark's bounds designated by "BookmarkName".
builder->Write(u"MySequence #");
auto fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bookmark's bounds.
// The paragraph that contains this field will show up in the TOC as an entry.
builder->Write(u"MySequence #");
fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// This SEQ field's sequence does not match the TOC's "TableOfFiguresLabel" property,
// and is within the bounds of the bookmark. Its paragraph will not show up in the TOC as an entry.
builder->Write(u"MySequence #");
fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bounds of the bookmark.
// This field also references another bookmark. The contents of that bookmark will appear in the TOC entry for this SEQ field.
// The SEQ field itself will not display the contents of that bookmark.
fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// Create a bookmark with contents that will show up in the TOC entry due to the above SEQ field referencing it.
builder->InsertBreak(BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.SEQ.Bookmark.docx");
```

## See Also

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
