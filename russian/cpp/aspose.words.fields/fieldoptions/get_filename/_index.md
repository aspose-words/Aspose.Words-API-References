---
title: "Aspose::Words::Fields::FieldOptions::get_FileName метод"
linktitle: "get_FileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldOptions::get_FileName. Получает или задает имя файла документа в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.fields/fieldoptions/get_filename/
---
## FieldOptions::get_FileName method


Получает или задает имя файла документа.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_FileName() const
```

## Примечания


Это свойство используется полем [FieldFileName](../../fieldfilename/) с более высоким приоритетом, чем свойство [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

## Примеры



Показывает, как использовать [FieldOptions](../) для переопределения значения по умолчанию для поля FILENAME.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// Это поле FILENAME будет отображать локальное системное имя файла загруженного документа.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// По умолчанию поле FILENAME показывает имя файла, но не полный локальный путь к нему в файловой системе.
// Мы можем установить флаг, чтобы он показывал полный путь к файлу.
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->set_IncludeFullPath(true);
field->Update();

ASSERT_EQ(get_MyDir() + u"Document.docx", field->get_Result());

// Мы также можем установить значение для этого свойства, чтобы
// переопределить значение, которое отображает поле FILENAME.
doc->get_FieldOptions()->set_FileName(u"FieldOptions.FILENAME.docx");
field->Update();

ASSERT_EQ(u" FILENAME  \\p", field->GetFieldCode());
ASSERT_EQ(u"FieldOptions.FILENAME.docx", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + doc->get_FieldOptions()->get_FileName());
```

## См. также

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
