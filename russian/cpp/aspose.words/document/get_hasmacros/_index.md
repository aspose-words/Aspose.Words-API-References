---
title: "Aspose::Words::Document::get_HasMacros метод"
linktitle: "get_HasMacros"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::get_HasMacros метод. Возвращает true, если документ содержит проект VBA (макросы) на C++."
type: docs
weight: 30000
url: /ru/cpp/aspose.words/document/get_hasmacros/
---
## Document::get_HasMacros method


Возвращает **true**, если в документе есть проект VBA (макросы).

```cpp
bool Aspose::Words::Document::get_HasMacros()
```


## Примеры



Показывает, как использовать поля MACROBUTTON, чтобы запускать макросы документа по щелчку.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// Вставьте поле MACROBUTTON и укажите один из макросов документа по имени в свойстве MacroName.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(System::String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// Используйте свойство для ссылки на \"ViewZoom200\", макрос, поставляемый с Microsoft Word.
// Мы можем найти все остальные макросы через View -> Macros (выпадающий список) -> View Macros.
// В этом меню выберите \"Word Commands\" из выпадающего списка \"Macros in:\".
// Если наш документ содержит пользовательский макрос с тем же именем, что и стандартный макрос,
// наш макрос будет тем, который запускает поле MACROBUTTON.
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(System::String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// Сохраните документ в типе, поддерживающем макросы.
doc->Save(get_ArtifactsDir() + u"Field.MACROBUTTON.docm");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
