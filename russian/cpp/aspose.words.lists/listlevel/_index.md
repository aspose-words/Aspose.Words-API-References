---
title: "Класс Aspose::Words::Lists::ListLevel"
linktitle: "ListLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Lists::ListLevel. Определяет форматирование уровня списка. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.lists/listlevel/
---
## ListLevel class


Определяет форматирование уровня списка. Чтобы узнать больше, посетите статью документации [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLevel : public Aspose::Words::IRunAttrSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [CreatePictureBullet](./createpicturebullet/)() | Создаёт форму графического маркера для текущего уровня списка. |
| [DeletePictureBullet](./deletepicturebullet/)() | Удаляет графический маркер для текущего уровня списка. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::ListLevel\>\&) | Сравнивает со указанным [ListLevel](./). |
| [get_Alignment](./get_alignment/)() const | Получает или задает выравнивание фактического номера элемента списка. |
| [get_CustomNumberStyleFormat](./get_customnumberstyleformat/)() | Получает или задает пользовательский формат стиля номера для этого уровня списка. Например: "a, ç, ĝ, ...". |
| [get_Font](./get_font/)() | Указывает форматирование символов, используемое для метки списка. |
| [get_ImageData](./get_imagedata/)() | Возвращает данные изображения формы пунктирного маркера для текущего уровня списка. |
| [get_IsLegal](./get_islegal/)() const | True, если уровень преобразует все унаследованные номера в арабские, false, если сохраняет их стиль номера. |
| [get_LinkedStyle](./get_linkedstyle/)() | Получает или задает стиль абзаца, связанный с этим уровнем списка. |
| [get_NumberFormat](./get_numberformat/)() const | Возвращает или задает формат номера для уровня списка. |
| [get_NumberPosition](./get_numberposition/)() const | Возвращает или задает позицию (в пунктах) номера или маркера для уровня списка. |
| [get_NumberStyle](./get_numberstyle/)() const | Возвращает или задает стиль номера для этого уровня списка. |
| [get_RestartAfterLevel](./get_restartafterlevel/)() const | Задает или возвращает уровень списка, который должен предшествовать указанному уровню списка, перезапускающему нумерацию. |
| [get_StartAt](./get_startat/)() | Возвращает или задает начальный номер для этого уровня списка. |
| [get_TabPosition](./get_tabposition/)() const | Возвращает или задает позицию табуляции (в пунктах) для уровня списка. |
| [get_TextPosition](./get_textposition/)() const | Возвращает или задает позицию (в пунктах) второй строки перенесённого текста для уровня списка. |
| [get_TrailingCharacter](./get_trailingcharacter/)() const | Возвращает или задает символ, вставляемый после номера для уровня списка. |
| static [GetEffectiveValue](./geteffectivevalue/)(int32_t, Aspose::Words::NumberStyle, const System::String\&) | Возвращает строковое представление объекта [ListLevel](./) для указанного индекса элемента списка. Параметры указывают [NumberStyle](../../aspose.words/numberstyle/) и необязательную строку формата, используемую, когда указано [Custom](../../aspose.words/numberstyle/). |
| [GetHashCode](./gethashcode/)() const override | Вычисляет хеш-код для этого объекта. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveTabStop](./removetabstop/)() | Удаляет табуляцию из уровня списка. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Lists::ListLevelAlignment) | Сеттер для [Aspose::Words::Lists::ListLevel::get_Alignment](./get_alignment/). |
| [set_CustomNumberStyleFormat](./set_customnumberstyleformat/)(const System::String\&) | Сеттер для [Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat](./get_customnumberstyleformat/). |
| [set_IsLegal](./set_islegal/)(bool) | Сеттер для [Aspose::Words::Lists::ListLevel::get_IsLegal](./get_islegal/). |
| [set_LinkedStyle](./set_linkedstyle/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Сеттер для [Aspose::Words::Lists::ListLevel::get_LinkedStyle](./get_linkedstyle/). |
| [set_NumberFormat](./set_numberformat/)(const System::String\&) | Сеттер для [Aspose::Words::Lists::ListLevel::get_NumberFormat](./get_numberformat/). |
| [set_NumberPosition](./set_numberposition/)(double) | Сеттер для [Aspose::Words::Lists::ListLevel::get_NumberPosition](./get_numberposition/). |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) | Сеттер для [Aspose::Words::Lists::ListLevel::get_NumberStyle](./get_numberstyle/). |
| [set_RestartAfterLevel](./set_restartafterlevel/)(int32_t) | Сеттер для [Aspose::Words::Lists::ListLevel::get_RestartAfterLevel](./get_restartafterlevel/). |
| [set_StartAt](./set_startat/)(int32_t) | Сеттер для [Aspose::Words::Lists::ListLevel::get_StartAt](./get_startat/). |
| [set_TabPosition](./set_tabposition/)(double) | Сеттер для [Aspose::Words::Lists::ListLevel::get_TabPosition](./get_tabposition/). |
| [set_TextPosition](./set_textposition/)(double) | Сеттер для [Aspose::Words::Lists::ListLevel::get_TextPosition](./get_textposition/). |
| [set_TrailingCharacter](./set_trailingcharacter/)(Aspose::Words::Lists::ListTrailingCharacter) | Сеттер для [Aspose::Words::Lists::ListLevel::get_TrailingCharacter](./get_trailingcharacter/). |
| static [Type](./type/)() |  |
## Примечания


Вы не создаёте объекты этого класса. Объекты уровней [List](../list/) создаются автоматически при создании списка. Вы получаете доступ к объектам [ListLevel](./) через коллекцию [ListLevelCollection](../listlevelcollection/).

Используйте свойства [ListLevel](./), чтобы задать форматирование списка для отдельных уровней списка.

## Примеры



Показывает, как применять пользовательское форматирование списка к абзацам при использовании [DocumentBuilder](../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
// Создайте список из шаблона Microsoft Word и настройте первые два уровня списка.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Это значение NumberFormat создаст символы маркеров в виде звёзд.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Создайте абзацы и примените к ним оба уровня нашего пользовательского форматирования списка.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## См. также

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
