---
title: "Aspose::Words::StyleCollection::Add метод"
linktitle: "Add"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::StyleCollection::Add метод. Создаёт новый пользовательский стиль и добавляет его в коллекцию в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/stylecollection/add/
---
## StyleCollection::Add method


Создает новый пользовательский стиль и добавляет его в коллекцию.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::Add(Aspose::Words::StyleType type, const System::String &name)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| type | Aspose::Words::StyleType | Значение [StyleType](../../styletype/), указывающее тип создаваемого стиля. |
| name | const System::String\& | Регистрозависимое имя создаваемого стиля. |
## Примечания


Вы можете создать символьный, абзацный или списокный стиль.

При создании стиля списка стиль создаётся с форматированием нумерованного списка по умолчанию (1 \\ a \\ i).

Выбрасывает исключение, если стиль с таким именем уже существует.

## Примеры



Показывает, как создать стиль списка и использовать его в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
// Мы можем включить целый объект List в стиль.
System::SharedPtr<Aspose::Words::Style> listStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle");

System::SharedPtr<Aspose::Words::Lists::List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// Измените внешний вид всех уровней списка в нашем списке.
for (auto&& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// Создайте другой список из списка внутри стиля.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// Добавьте несколько элементов списка, которые наш список будет форматировать.
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// Создайте и примените другой список на основе стиля списка.
System::SharedPtr<Aspose::Words::Lists::List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateAndUseListStyle.docx");
```


Показывает, как добавить [Style](../../style/) в коллекцию стилей документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Установите параметры по умолчанию для новых стилей, которые мы позже можем добавить в эту коллекцию.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Если мы добавим стиль типа "StyleType.Paragraph", коллекция применит значения
// его свойство "DefaultParagraphFormat" к свойству "ParagraphFormat" стиля.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Добавьте стиль и затем проверьте, что у него установлены настройки по умолчанию.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## См. также

* Class [Style](../../style/)
* Enum [StyleType](../../styletype/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
