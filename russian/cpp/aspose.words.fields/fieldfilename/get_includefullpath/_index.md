---
title: "Метод Aspose::Words::Fields::FieldFileName::get_IncludeFullPath"
linktitle: "get_IncludeFullPath"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldFileName::get_IncludeFullPath. Получает или задает, следует ли включать полное имя пути к файлу в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldfilename/get_includefullpath/
---
## FieldFileName::get_IncludeFullPath method


Получает или задает, следует ли включать полное имя пути к файлу.

```cpp
bool Aspose::Words::Fields::FieldFileName::get_IncludeFullPath()
```


## Примеры



Показывает, как использовать [FieldOptions](../../fieldoptions/) для переопределения значения по умолчанию для поля FILENAME.
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

* Class [FieldFileName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
