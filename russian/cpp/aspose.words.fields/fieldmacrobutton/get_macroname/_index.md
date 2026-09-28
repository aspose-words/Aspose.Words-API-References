---
title: "Метод Aspose::Words::Fields::FieldMacroButton::get_MacroName"
linktitle: "get_MacroName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldMacroButton::get_MacroName метод. Получает или задает имя макроса или команды для выполнения в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fields/fieldmacrobutton/get_macroname/
---
## FieldMacroButton::get_MacroName method


Получает или задает имя макроса или команды для запуска.

```cpp
System::String Aspose::Words::Fields::FieldMacroButton::get_MacroName()
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

* Class [FieldMacroButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
