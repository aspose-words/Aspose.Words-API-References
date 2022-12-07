---
title: get_IsInKilobytes
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether to display the file size in kilobytes.
type: docs
weight: 14
url: /cpp/aspose.words.fields/fieldfilesize/get_isinkilobytes/
---
## FieldFileSize::get_IsInKilobytes method


Gets or sets whether to display the file size in kilobytes.

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes()
```


## Examples



Shows how to display the file size of a document with a FILESIZE field. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = MakeObject<DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// Below are three different units of measure
// with which FILESIZE fields can display the document's file size.
// 1 -  Bytes:
auto field = System::DynamicCast<FieldFileSize>(builder->InsertField(FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  Kilobytes:
builder->InsertParagraph();
field = System::DynamicCast<FieldFileSize>(builder->InsertField(FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  Megabytes:
builder->InsertParagraph();
field = System::DynamicCast<FieldFileSize>(builder->InsertField(FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// To update the values of these fields while editing in Microsoft Word,
// we must first save the changes, and then manually update these fields.
doc->Save(ArtifactsDir + u"Field.FILESIZE.docx");
```

## See Also

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
