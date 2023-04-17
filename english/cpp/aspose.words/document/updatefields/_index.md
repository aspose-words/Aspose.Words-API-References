---
title: Aspose::Words::Document::UpdateFields method
linktitle: UpdateFields
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::UpdateFields method. Updates the values of fields in the whole document in C++.'
type: docs
weight: 96000
url: /cpp/aspose.words/document/updatefields/
---
## Document::UpdateFields method


Updates the values of fields in the whole document.

```cpp
void Aspose::Words::Document::UpdateFields()
```

## Remarks


When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact. Therefore, you would usually want to call this method before saving if you have modified the document programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF). The page layout-related fields are updated when you render a document or call [UpdatePageLayout](../updatepagelayout/).

Use the [NormalizeFieldTypes](../normalizefieldtypes/) method before fields updating if there were document changes that affected field types.

To update fields in a specific part of the document use [UpdateFields](../../range/updatefields/).

## Examples



Shows how to insert a Table of contents (TOC) into a document using heading styles as entries. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a table of contents for the first page of the document.
// Configure the table to pick up paragraphs with headings of levels 1 to 3.
// Also, set its entries to be hyperlinks that will take us
// to the location of the heading when left-clicked in Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(BreakType::PageBreak);

// Populate the table of contents by adding paragraphs with heading styles.
// Each such heading with a level between 1 and 3 will create an entry in the table.
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// A table of contents is a field of a type that needs to be updated to show an up-to-date result.
doc->UpdateFields();
doc->Save(ArtifactsDir + u"DocumentBuilder.InsertToc.docx");
```


Shows to use the QUOTE field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a QUOTE field, which will display the value of its Text property.
auto field = System::DynamicCast<FieldQuote>(builder->InsertField(FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Insert a QUOTE field and nest a DATE field inside it.
// DATE fields update their value to the current date every time we open the document using Microsoft Word.
// Nesting the DATE field inside the QUOTE field like this will freeze its value
// to the date when we created the document.
builder->Write(u"\nDocument creation date: ");
field = System::DynamicCast<FieldQuote>(builder->InsertField(FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(FieldType::FieldDate, true);

ASSERT_EQ(String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Update all the fields to display their correct results.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(ArtifactsDir + u"Field.QUOTE.docx");
```


Shows how to set user details, and display them using fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a UserInformation object and set it as the data source for fields that display user information.
auto userInformation = MakeObject<UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
// the respective properties of the UserInformation object that we have created above.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// The field options object also has a static default user that fields from all documents can refer to.
UserInformation::get_DefaultUser()->set_Name(u"Default User");
UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"FieldOptions.CurrentUser.docx");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
