---
title: Aspose::Words::Fields::FieldFileName::get_IncludeFullPath method
linktitle: get_IncludeFullPath
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldFileName::get_IncludeFullPath method. Gets or sets whether to include the full file path name in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldfilename/get_includefullpath/
---
## FieldFileName::get_IncludeFullPath method


Gets or sets whether to include the full file path name.

```cpp
bool Aspose::Words::Fields::FieldFileName::get_IncludeFullPath()
```


## Examples



Shows how to use [FieldOptions](../../fieldoptions/) to override the default value for the FILENAME field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// This FILENAME field will display the local system file name of the document we loaded.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// By default, the FILENAME field shows the file's name, but not its full local file system path.
// We can set a flag to make it show the full file path.
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
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
