---
title: "Класс Aspose::Words::Lists::List"
linktitle: "Список"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Lists::List. Представляет форматирование списка. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.lists/list/
---
## List class


Представляет форматирование списка. Чтобы узнать больше, посетите статью документации [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class List : public System::IComparable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [CompareTo](./compareto/)(System::SharedPtr\<Aspose::Words::Lists::List\>) override | Сравнивает указанный список с текущим списком. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Сравнивает с указанным списком. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_Document](./get_document/)() const | Получает документ‑владельца. |
| [get_IsListStyleDefinition](./get_isliststyledefinition/)() | Возвращает **true**, если этот список является определением стиля списка. |
| [get_IsListStyleReference](./get_isliststylereference/)() | Возвращает **true**, если этот список является ссылкой на стиль списка. |
| [get_IsMultiLevel](./get_ismultilevel/)() | Возвращает **true**, когда список содержит 9 уровней; **false**, когда 1 уровень. |
| [get_IsRestartAtEachSection](./get_isrestartateachsection/)() | Указывает, следует ли перезапускать список в каждом разделе. Значение по умолчанию — **false**. |
| [get_ListId](./get_listid/)() const | Получает уникальный идентификатор списка. |
| [get_ListLevels](./get_listlevels/)() | Получает коллекцию уровней списка для данного списка. |
| [get_Style](./get_style/)() | Получает стиль списка, на который этот список ссылается или который определяет. |
| [GetHashCode](./gethashcode/)() const override | Вычисляет хеш‑код для этого объекта списка. |
| [GetType](./gettype/)() const override |  |
| [HasSameTemplate](./hassametemplate/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Возвращает true, если текущий список и указанный список созданы из одного шаблона. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsRestartAtEachSection](./set_isrestartateachsection/)(bool) | Сеттер для [Aspose::Words::Lists::List::get_IsRestartAtEachSection](./get_isrestartateachsection/). |
| static [Type](./type/)() |  |
## Примечания


Список в документе Microsoft Word представляет собой набор свойств форматирования списка. Каждый список может иметь до 9 уровней, а свойства форматирования, такие как стиль нумерации, начальное значение, отступ, позиция табуляции и т.д., определяются отдельно для каждого уровня.

Объект [List](./) всегда принадлежит коллекции [ListCollection](../listcollection/).

Чтобы создать новый список, используйте методы Add коллекции [ListCollection](../listcollection/).

Чтобы изменить форматирование списка, используйте объекты [ListLevel](../listlevel/), найденные в коллекции [ListLevels](./get_listlevels/).

Чтобы применить или удалить форматирование списка в абзаце, используйте [ListFormat](../listformat/).

## Примеры



Показывает, как работать с уровнями списка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
// Ниже представлены два типа списков, которые мы можем создать с помощью document builder.
// 1 -  Нумерованный список:
// Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Установив свойство \"ListLevelNumber\", мы можем увеличить уровень списка
// чтобы начать автономный подсписок в текущем элементе списка.
// Шаблон списка Microsoft Word под названием \"NumberDefault\" использует цифры для создания уровней списка для первого уровня списка.
// Более глубокие уровни списка используют буквы и римские цифры в нижнем регистре.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Маркированный список:
// Этот список будет применять отступ и символ маркера (\"•\") перед каждым абзацем.
// Более глубокие уровни этого списка будут использовать разные символы, такие как \"■\" и \"○\".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Мы можем отключить форматирование списка, чтобы не форматировать последующие абзацы как списки, сняв флаг \"List\".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


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


Показывает, как перезапустить нумерацию в списке, скопировав список.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
// Создайте список из шаблона Microsoft Word и настройте его первый уровень списка.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Примените наш список к некоторым абзацам.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Мы можем добавить копию существующего списка в коллекцию списков документа
// чтобы создать похожий список без изменения оригинала.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Примените второй список к новым абзацам.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## См. также

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
