---
title: Aspose::Words::Fields::FieldFileName::set_IncludeFullPath method
linktitle: set_IncludeFullPath
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldFileName::set_IncludeFullPath method. Sets whether to include the full file path name in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fields/fieldfilename/set_includefullpath/
---
## FieldFileName::set_IncludeFullPath method


Sets whether to include the full file path name.

```cpp
void Aspose::Words::Fields::FieldFileName::set_IncludeFullPath(bool value)
```

## Examples


Shows how to use FieldOptions to override the default value for the FILENAME field.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// This FILENAME field will display the local system file name of the document we loaded.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// By default, the FILENAME field shows the file's name, but not its full local file system path.
// We can set a flag to make it show the full file path.
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(FieldType::FieldFileName, true));
field->set_IncludeFullPath(true);
field->Update();

ASSERT_EQ(get_MyDir() + u"Document.docx", field->get_Result());

// We can also set a value for this property to
// override the value that the FILENAME field displays.
doc->get_FieldOptions()->set_FileName(u"FieldOptions.FILENAME.docx");
field->Update();

ASSERT_EQ(u" FILENAME  \\p", field->GetFieldCode());
ASSERT_EQ(u"FieldOptions.FILENAME.docx", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + doc->get_FieldOptions()->get_FileName());
```
## See Also

* Class [FieldFileName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
