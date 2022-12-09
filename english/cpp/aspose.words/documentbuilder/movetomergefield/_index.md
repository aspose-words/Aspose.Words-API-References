---
title: MoveToMergeField
second_title: Aspose.Words for C++ API Reference
description: Moves the cursor to a position just beyond the specified merge field and removes the merge field.
type: docs
weight: 742
url: /cpp/aspose.words/documentbuilder/movetomergefield/
---
## DocumentBuilder::MoveToMergeField(const System::String\&) method


Moves the cursor to a position just beyond the specified merge field and removes the merge field.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | const System::String\& | The case-insensitive name of the mail merge field. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.
## Remarks


Note that this method deletes the merge field from the document after moving the cursor.

## Examples



Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
// and then fill them manually.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(ArtifactsDir + u"DocumentBuilder.FillMergeFields.docx");
```

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::MoveToMergeField(const System::String\&, bool, bool) method


Moves the merge field to the specified merge field.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName, bool isAfter, bool isDeleteField)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | const System::String\& | The case-insensitive name of the mail merge field. |
| isAfter | bool | When **true**, moves the cursor to be after the field end. When **false**, moves the cursor to be before the field start. |
| isDeleteField | bool | When **true**, deletes the merge field. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.

## Examples



Shows how to insert fields, and move the document builder's cursor to them. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// Move the cursor to the first MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// If we wish to edit the field's field code or contents using the builder,
// its cursor would need to be inside a field.
// To place it inside a field, we would need to call the document builder's MoveTo method
// and pass the field's start or separator node as an argument.
builder->Write(u" Text between our merge fields. ");

doc->Save(ArtifactsDir + u"DocumentBuilder.MergeFields.docx");
```

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
