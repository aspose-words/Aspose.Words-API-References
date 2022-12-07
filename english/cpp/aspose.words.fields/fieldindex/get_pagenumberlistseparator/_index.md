---
title: get_PageNumberListSeparator
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the character sequence that is used to separate two page numbers in a page number list.
type: docs
weight: 131
url: /cpp/aspose.words.fields/fieldindex/get_pagenumberlistseparator/
---
## FieldIndex::get_PageNumberListSeparator method


Gets or sets the character sequence that is used to separate two page numbers in a page number list.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_PageNumberListSeparator()
```


## Examples



Shows how to edit the page number separator in an INDEX field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create an INDEX field which will display an entry for each XE field found in the document.
// Each entry will display the XE field's Text property value on the left side,
// and the number of the page that contains the XE field on the right.
// The INDEX entry will group XE fields with matching values in the "Text" property
// into one entry as opposed to making an entry for each XE field.
auto index = System::DynamicCast<FieldIndex>(builder->InsertField(FieldType::FieldIndex, true));

// If our INDEX field has an entry for a group of XE fields,
// this entry will display the number of each page that contains an XE field that belongs to this group.
// We can set custom separators to customize the appearance of these page numbers.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageNumberListSeparator(u" & ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\l \" & \"", index->GetFieldCode());
ASSERT_TRUE(index->get_HasPageNumberSeparator());

// After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
builder->InsertBreak(BreakType::PageBreak);
auto indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

ASSERT_EQ(u" XE  \"First entry\"", indexEntry->GetFieldCode());

builder->InsertBreak(BreakType::PageBreak);
indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

builder->InsertBreak(BreakType::PageBreak);
indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.INDEX.XE.PageNumberList.docx");
```

## See Also

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
