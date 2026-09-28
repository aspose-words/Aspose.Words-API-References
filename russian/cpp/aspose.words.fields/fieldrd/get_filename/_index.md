---
title: "Метод Aspose::Words::Fields::FieldRD::get_FileName"
linktitle: "get_FileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldRD::get_FileName. Получает или задает имя файла, который следует включить при генерации оглавления, списка источников или указателя в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldrd/get_filename/
---
## FieldRD::get_FileName method


Получает или задает имя файла, который следует включать при создании оглавления, списка источников или указателя.

```cpp
System::String Aspose::Words::Fields::FieldRD::get_FileName()
```


## Примеры



Показывает, как использовать поле RD для создания записей оглавления из заголовков в других документах.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Используйте построитель документа для вставки оглавления,
// а затем добавить одну запись в оглавление на следующей странице.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
builder->Writeln(u"TOC entry from within this document");

// Вставьте поле RD, которое ссылается на другой документ локальной файловой системы в его свойстве FileName.
// Оглавление теперь также будет принимать все заголовки из ссылочного документа в качестве записей в своей таблице.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRD>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRefDoc, true));
field->set_FileName(get_ArtifactsDir() + u"ReferencedDocument.docx");

ASSERT_EQ(System::String::Format(u" RD  {0}ReferencedDocument.docx", get_ArtifactsDir().Replace(u"\\", u"\\\\")), field->GetFieldCode());

// Создайте документ, на который ссылается поле RD, и вставьте заголовок.
// Этот заголовок появится в виде записи в поле Оглавления в нашем первом документе.
auto referencedDoc = System::MakeObject<Aspose::Words::Document>();
auto refDocBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(referencedDoc);
refDocBuilder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
refDocBuilder->Writeln(u"TOC entry from referenced document");
referencedDoc->Save(get_ArtifactsDir() + u"ReferencedDocument.docx");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.RD.docx");
```

## См. также

* Class [FieldRD](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
