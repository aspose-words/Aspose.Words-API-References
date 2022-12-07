---
title: get_EntryType
second_title: Aspose.Words for C++ API Reference
description: Gets or sets an index entry type.
type: docs
weight: 14
url: /cpp/aspose.words.fields/fieldxe/get_entrytype/
---
## FieldXE::get_EntryType method


Gets or sets an index entry type.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_EntryType()
```


## Examples



Shows how to create an INDEX field, and then use XE fields to populate it with entries. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create an INDEX field which will display an entry for each XE field found in the document.
// Each entry will display the XE field's Text property value on the left side
// and the page containing the XE field on the right.
// If the XE fields have the same value in their "Text" property,
// the INDEX field will group them into one entry.
auto index = System::DynamicCast<FieldIndex>(builder->InsertField(FieldType::FieldIndex, true));

// Configure the INDEX field only to display XE fields that are within the bounds
// of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
// For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// On a new page, start the bookmark with a name that matches the value
// of the INDEX field's "BookmarkName" property.
builder->InsertBreak(BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// The INDEX field will pick up this entry because it is inside the bookmark,
// and its entry type also matches the INDEX field's entry type.
auto indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Insert an XE field that will not appear in the INDEX because the entry types do not match.
builder->InsertBreak(BreakType::PageBreak);
indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// End the bookmark and insert an XE field afterwards.
// It is of the same type as the INDEX field, but will not appear
// since it is outside the bookmark's boundaries.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(BreakType::PageBreak);
indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.INDEX.XE.Filtering.docx");
```

## See Also

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
