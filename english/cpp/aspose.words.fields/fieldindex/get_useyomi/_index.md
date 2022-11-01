---
title: get_UseYomi
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether to enable the use of yomi text for index entries.
type: docs
weight: 196
url: /cpp/aspose.words.fields/fieldindex/get_useyomi/
---
## FieldIndex.get_UseYomi method


Gets or sets whether to enable the use of yomi text for index entries.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_UseYomi()
```


## Examples




Shows how to sort INDEX field entries phonetically. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create an INDEX field which will display an entry for each XE field found in the document.
// Each entry will display the XE field's Text property value on the left side,
// and the number of the page that contains the XE field on the right.
// The INDEX entry will collect all XE fields with matching values in the "Text" property
// into one entry as opposed to making an entry for each XE field.
auto index = System::DynamicCast<FieldIndex>(builder->InsertField(FieldType::FieldIndex, true));

// The INDEX table automatically sorts its entries by the values of their Text properties in alphabetic order.
// Set the INDEX table to sort entries phonetically using Hiragana instead.
index->set_UseYomi(sortEntriesUsingYomi);

if (sortEntriesUsingYomi)
{
    ASSERT_EQ(u" INDEX  \\y", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX ", index->GetFieldCode());
}

// Insert 4 XE fields, which would show up as entries in the INDEX field's table of contents.
// The "Text" property may contain a word's spelling in Kanji, whose pronunciation may be ambiguous,
// while the "Yomi" version of the word will spell exactly how it is pronounced using Hiragana.
// If we set our INDEX field to use Yomi, it will sort these entries
// by the value of their Yomi properties, instead of their Text values.
builder->InsertBreak(BreakType::PageBreak);
auto indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛子");
indexEntry->set_Yomi(u"あ");

ASSERT_EQ(u" XE  愛子 \\y あ", indexEntry->GetFieldCode());

builder->InsertBreak(BreakType::PageBreak);
indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"明美");
indexEntry->set_Yomi(u"あ");

builder->InsertBreak(BreakType::PageBreak);
indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"恵美");
indexEntry->set_Yomi(u"え");

builder->InsertBreak(BreakType::PageBreak);
indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛美");
indexEntry->set_Yomi(u"え");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.INDEX.XE.Yomi.docx");
```

