---
title: get_HasSequenceName
second_title: Aspose.Words for C++ API Reference
description: Gets a value indicating whether a sequence should be used while the field's result building.
type: docs
weight: 66
url: /cpp/aspose.words.fields/fieldindex/get_hassequencename/
---
## FieldIndex::get_HasSequenceName method


Gets a value indicating whether a sequence should be used while the field's result building.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_HasSequenceName()
```


## Examples



Shows how to split a document into portions by combining INDEX and SEQ fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create an INDEX field which will display an entry for each XE field found in the document.
// Each entry will display the XE field's Text property value on the left side,
// and the number of the page that contains the XE field on the right.
// If the XE fields have the same value in their "Text" property,
// the INDEX field will group them into one entry.
auto index = System::DynamicCast<FieldIndex>(builder->InsertField(FieldType::FieldIndex, true));

// In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
// the number that the sequence count is on at the XE field location that created this entry.
index->set_SequenceName(u"MySequence");

// Set text that will around the sequence and page numbers to explain their meaning to the user.
// An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
// PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
index->set_PageNumberSeparator(u"\tMySequence at ");
index->set_SequenceSeparator(u" on page ");
ASSERT_TRUE(index->get_HasSequenceName());

ASSERT_EQ(u" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index->GetFieldCode());

// SEQ fields display a count that increments at each SEQ field.
// These fields also maintain separate counts for each unique named sequence
// identified by the SEQ field's "SequenceIdentifier" property.
// Insert a SEQ field which moves the "MySequence" sequence to 1.
// This field no different from normal document text. It will not appear on an INDEX field's table of contents.
builder->InsertBreak(BreakType::PageBreak);
auto sequenceField = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", sequenceField->GetFieldCode());

// Insert an XE field which will create an entry in the INDEX field.
// Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
// this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
auto indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

ASSERT_EQ(u" XE  Cat", indexEntry->GetFieldCode());

// Insert a page break and use SEQ fields to advance "MySequence" to 3.
builder->InsertBreak(BreakType::PageBreak);
sequenceField = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");
sequenceField = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

// Insert an XE field with the same Text property as the one above.
// The INDEX entry will group XE fields with matching values in the "Text" property
// into one entry as opposed to making an entry for each XE field.
// Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
// The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

// Insert an XE field with a new and unique Text property value.
// This will add a new entry, with MySequence at 3 on page 4.
builder->InsertBreak(BreakType::PageBreak);
indexEntry = System::DynamicCast<FieldXE>(builder->InsertField(FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Dog");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.INDEX.XE.Sequence.docx");
```

## See Also

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
