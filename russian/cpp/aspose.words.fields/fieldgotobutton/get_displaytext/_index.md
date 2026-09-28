---
title: "Метод Aspose::Words::Fields::FieldGoToButton::get_DisplayText"
linktitle: "get_DisplayText"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldGoToButton::get_DisplayText. Получает или задает текст \"кнопки\", который появляется в документе, чтобы его можно было выбрать для активации перехода в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldgotobutton/get_displaytext/
---
## FieldGoToButton::get_DisplayText method


Получает или задает текст "кнопки", который появляется в документе, чтобы её можно было выбрать для активации перехода.

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_DisplayText()
```


## Примеры



Показывает, как вставить поле GOTOBUTTON.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавьте поле GOTOBUTTON. Когда мы дважды щёлкнем это поле в Microsoft Word,
// курсор текста переместится к закладке, имя которой указывает свойство Location.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// Вставьте действительную закладку, на которую будет ссылаться поле.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```

## См. также

* Class [FieldGoToButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
