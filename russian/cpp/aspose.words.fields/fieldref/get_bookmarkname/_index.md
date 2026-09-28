---
title: "Aspose::Words::Fields::FieldRef::get_BookmarkName метод"
linktitle: "Метод Aspose::Words::Fields::FieldAsk::set_DefaultResponse"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldRef::get_BookmarkName метод. Получает или задает имя ссылочной закладки в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldref/get_bookmarkname/
---
## FieldRef::get_BookmarkName method


Получает или задает имя ссылочной закладки.

```cpp
System::String Aspose::Words::Fields::FieldRef::get_BookmarkName()
```


## Примеры



Показывает, как создать текст с закладкой с помощью поля SET, а затем отобразить его в документе с помощью поля REF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Назовите текст с закладкой с помощью поля SET.
// Это поле ссылается на \"bookmark\", а не на структуру закладки, которая появляется в тексте, а на именованную переменную.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Обратитесь к закладке по имени в поле REF и отобразите её содержимое.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## См. также

* Class [FieldRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
