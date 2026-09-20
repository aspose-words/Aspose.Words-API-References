---
title: "Метод Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes"
linktitle: "get_IsInMegabytes"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes. Получает или задает, отображать ли размер файла в мегабайтах в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fields/fieldfilesize/get_isinmegabytes/
---
## FieldFileSize::get_IsInMegabytes method


Получает или задаёт, отображать ли размер файла в мегабайтах.

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes()
```


## Примеры



Показывает, как отобразить размер файла документа с помощью поля FILESIZE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// Ниже представлены три различных единицы измерения
// с помощью которых поля FILESIZE могут отображать размер файла документа.
// 1 -  Байт:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  Килобайт:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  Мегабайт:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// Чтобы обновить значения этих полей при редактировании в Microsoft Word,
// мы должны сначала сохранить изменения, а затем вручную обновить эти поля.
doc->Save(get_ArtifactsDir() + u"Field.FILESIZE.docx");
```

## См. также

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
