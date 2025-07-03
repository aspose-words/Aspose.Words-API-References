---
title: Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes method
linktitle: get_IsInMegabytes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes method. Gets or sets whether to display the file size in megabytes in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fields/fieldfilesize/get_isinmegabytes/
---
## FieldFileSize::get_IsInMegabytes method


Gets or sets whether to display the file size in megabytes.

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes()
```


## Examples



Shows how to display the file size of a document with a FILESIZE field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// Below are three different units of measure
// with which FILESIZE fields can display the document's file size.
// 1 -  Bytes:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  Kilobytes:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  Megabytes:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// To update the values of these fields while editing in Microsoft Word,
// we must first save the changes, and then manually update these fields.
doc->Save(get_ArtifactsDir() + u"Field.FILESIZE.docx");
```

## See Also

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
