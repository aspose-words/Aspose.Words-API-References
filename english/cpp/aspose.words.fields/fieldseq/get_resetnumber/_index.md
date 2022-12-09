---
title: get_ResetNumber
second_title: Aspose.Words for C++ API Reference
description: Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent.
type: docs
weight: 53
url: /cpp/aspose.words.fields/fieldseq/get_resetnumber/
---
## FieldSeq::get_ResetNumber method


Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_ResetNumber()
```


## Examples



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
auto fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Display the next number in this sequence with another SEQ field.
builder->Write(u", #");
fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
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
fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// The above heading is a level 1 heading, so the count for this sequence is reset to 1.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Move to the next number of this sequence.
builder->Write(u", #");
fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.SEQ.ResetNumbering.docx");
```

## See Also

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
