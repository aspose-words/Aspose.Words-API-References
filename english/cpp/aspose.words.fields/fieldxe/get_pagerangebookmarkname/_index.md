---
title: get_PageRangeBookmarkName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number.
type: docs
weight: 53
url: /cpp/aspose.words.fields/fieldxe/get_pagerangebookmarkname/
---
## FieldXE::get_PageRangeBookmarkName method


Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName()
```


## Examples



Shows how to specify a bookmark's spanned pages as a page range for an INDEX field entry. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create an INDEX field which will display an entry for each XE field found in the document.
// Each entry will display the XE field's Text property value on the left side,
// and the number of the page that contains the XE field on the right.
// The INDEX entry will collect all XE fields with matching values in the "Text" property
// into one entry as opposed to making an entry for each XE field.
auto index = System::DynamicCast<FieldIndex>(builder->InsertField(FieldType::FieldIndex, true));

// For INDEX entries that display page ranges, we can specify a separator string
// which will appear between the number of the first page, and the number of the last.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageRangeSeparator(u" to ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\g \" to \"", index->GetFieldCode());

builder->InsertBreak(BreakType::PageBreak);
auto indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"My entry");

// If an XE field names a bookmark using the PageRangeBookmarkName property,
// its INDEX entry will show the range of pages that the bookmark spans
// instead of the number of the page that contains the XE field.
indexEntry->set_PageRangeBookmarkName(u"MyBookmark");

ASSERT_EQ(u" XE  \"My entry\" \\r MyBookmark", indexEntry->GetFieldCode());
ASSERT_EQ(u"MyBookmark", indexEntry->get_PageRangeBookmarkName());

// Insert a bookmark that starts on page 3 and ends on page 5.
// The INDEX entry for the XE field that references this bookmark will display this page range.
// In our table, the INDEX entry will display "My entry, on page(s) 3 to 5".
builder->InsertBreak(BreakType::PageBreak);
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Start of MyBookmark");
builder->InsertBreak(BreakType::PageBreak);
builder->InsertBreak(BreakType::PageBreak);
builder->Write(u"End of MyBookmark");
builder->EndBookmark(u"MyBookmark");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.INDEX.XE.PageRangeBookmark.docx");
```

## See Also

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
