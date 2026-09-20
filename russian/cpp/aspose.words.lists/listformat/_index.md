---
title: "Класс Aspose::Words::Lists::ListFormat"
linktitle: "ListFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Lists::ListFormat. Позволяет управлять тем, какое форматирование списка применяется к абзацу. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.lists/listformat/
---
## ListFormat class


Позволяет контролировать, какое форматирование списка применяется к абзацу. Чтобы узнать больше, посетите статью документации [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListFormat : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [ApplyBulletDefault](./applybulletdefault/)() | Создаёт новый стандартный маркированный список и применяет его к абзацу. |
| [ApplyNumberDefault](./applynumberdefault/)() | Начинает новый список с нумерацией по умолчанию и применяет его к абзацу. |
| [get_IsListItem](./get_islistitem/)() | Истина, когда к абзацу применено маркированное или нумерованное форматирование. |
| [get_List](./get_list/)() | Получает или задает список, членом которого является данный абзац. |
| [get_ListLevel](./get_listlevel/)() | Возвращает форматирование уровня списка плюс любые переопределения форматирования, применённые к текущему абзацу. |
| [get_ListLevelNumber](./get_listlevelnumber/)() | Получает или задает номер уровня списка (от 0 до 8) для абзаца. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ListIndent](./listindent/)() | Увеличивает уровень списка текущего абзаца на один уровень. |
| [ListOutdent](./listoutdent/)() | Уменьшает уровень списка текущего абзаца на один уровень. |
| [RemoveNumbers](./removenumbers/)() | Удаляет номера или маркеры из текущего абзаца и устанавливает уровень списка в ноль. |
| [set_List](./set_list/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Сеттер для [Aspose::Words::Lists::ListFormat::get_List](./get_list/). |
| [set_ListLevelNumber](./set_listlevelnumber/)(int32_t) | Сеттер для [Aspose::Words::Lists::ListFormat::get_ListLevelNumber](./get_listlevelnumber/). |
| static [Type](./type/)() |  |
## Примечания


Абзац в документе Microsoft Word может быть маркированным или нумерованным. Когда абзац маркирован или нумерован, говорят, что к абзацу применено форматирование списка.

Вы не создаёте объекты класса [ListFormat](./) напрямую. Вы получаете доступ к [ListFormat](./) как к свойству другого объекта, который может иметь связанное форматирование списка. В данный момент объектами, которые могут иметь форматирование списка, являются: [Paragraph](../../aspose.words/paragraph/), [Style](../../aspose.words/style/) и [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

Само форматирование списка хранится внутри объекта [List](../list/), который хранится отдельно от абзацев. Объекты списков хранятся внутри коллекции [ListCollection](../listcollection/). Для каждого [Document](../../aspose.words/document/) существует единственная коллекция [ListCollection](../listcollection/).

Абзацы физически не принадлежат списку. Абзацы лишь ссылаются на конкретный объект списка через свойство [List](./get_list/) и на конкретный уровень в списке через свойство [ListLevelNumber](./get_listlevelnumber/). Устанавливая эти два свойства, вы контролируете, какие маркеры и нумерация применяются к абзацу.

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

## См. также

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
