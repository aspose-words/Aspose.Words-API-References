---
title: "Aspose::Words::Lists::ListCollection class"
linktitle: "ListCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::ListCollection class. Хранит и управляет форматированием маркированных и нумерованных списков, используемых в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.lists/listcollection/
---
## ListCollection class


Хранит и управляет форматированием маркированных и нумерованных списков, используемых в документе. Чтобы узнать больше, посетите статью документации [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(Aspose::Words::Lists::ListTemplate) | Создаёт новый список на основе предопределённого шаблона и добавляет его в коллекцию списков в документе. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Создаёт новый список, который ссылается на стиль списка, и добавляет его в коллекцию списков в документе. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Создаёт новый список, копируя указанный список, и добавляет его в коллекцию списков в документе. |
| [AddSingleLevelList](./addsinglelevellist/)(Aspose::Words::Lists::ListTemplate) | Создаёт новый одноуровневый список на основе предопределённого шаблона и добавляет его в коллекцию списков в документе. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Получает количество нумерованных и маркированных списков в документе. |
| [get_Document](./get_document/)() const | Получает документ‑владельца. |
| [GetEnumerator](./getenumerator/)() override | Получает объект‑перечислитель, который будет перечислять списки в документе. |
| [GetListByListId](./getlistbylistid/)(int32_t) | Получает список по идентификатору списка. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает список по индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Типовое определение | Описание |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Примечания


Список в документе Microsoft Word представляет собой набор свойств форматирования списка. Форматирование списков хранится в коллекции [ListCollection](./) отдельно от абзацев текста.

Вы не создаёте объекты этого класса. В документе всегда существует только один объект [ListCollection](./), доступный через свойство [Lists](../../aspose.words/documentbase/get_lists/).

Чтобы создать новый список на основе предопределённого шаблона списка или стиля списка, используйте метод [Add()](../).

Чтобы создать новый список с форматированием, идентичным существующему списку, используйте метод [AddCopy()](../).

Чтобы сделать абзац маркированным или нумерованным, необходимо применить форматирование списка к абзацу, присвоив объект [List](../list/) свойству [List](../listformat/get_list/) объекта [ListFormat](../listformat/).

Чтобы удалить форматирование списка из абзаца, используйте метод [RemoveNumbers](../listformat/removenumbers/).

Если вы немного знакомы с WordprocessingML, то, вероятно, знаете, что он определяет отдельные понятия «list» и «list definition». Это точно соответствует тому, как форматирование списка хранится в документе Microsoft Word на низком уровне. Определение [List](../list/) похоже на «схему», а список — на экземпляр определения списка.

Чтобы упростить модель программирования, Aspose.Words скрывает различие между списком и определением списка так же, как Microsoft Word скрывает его в пользовательском интерфейсе. Это позволяет вам больше сосредоточиться на том, как должен выглядеть ваш документ, а не на построении низкоуровневых объектов для удовлетворения требований формата файлов Microsoft Word.

В текущей версии [Aspose.Words](../../aspose.words/) невозможно удалить списки после их создания. Это аналогично Microsoft Word, где пользователь не имеет явного контроля над определениями списков.

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
