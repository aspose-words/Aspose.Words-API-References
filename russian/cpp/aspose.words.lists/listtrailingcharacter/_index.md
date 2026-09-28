---
title: "Перечисление Aspose::Words::Lists::ListTrailingCharacter"
linktitle: "ListTrailingCharacter"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Lists::ListTrailingCharacter. Указывает символ, который разделяет метку списка и текст абзаца в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.lists/listtrailingcharacter/
---
## ListTrailingCharacter enum


Указывает символ, разделяющий метку списка и текст абзаца.

```cpp
enum class ListTrailingCharacter
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Таб | 0 | Символ табуляции размещается между меткой списка и текстом абзаца. |
| Пробел | 1 | Символ пробела размещается между меткой списка и текстом абзаца. |
| Ничего | 2 | Нет символа-разделителя между меткой списка и текстом абзаца. |

## Примечания


Используется как значение свойства [TrailingCharacter](../listlevel/get_trailingcharacter/).

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
