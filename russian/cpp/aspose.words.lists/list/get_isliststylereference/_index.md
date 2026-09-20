---
title: "Aspose::Words::Lists::List::get_IsListStyleReference метод"
linktitle: "get_IsListStyleReference"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::List::get_IsListStyleReference метод. Возвращает true, если этот список является ссылкой на стиль списка в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.lists/list/get_isliststylereference/
---
## List::get_IsListStyleReference method


Возвращает **true**, если этот список является ссылкой на стиль списка.

```cpp
bool Aspose::Words::Lists::List::get_IsListStyleReference()
```

## Примечания


Примечание, изменение свойств списка, который является ссылкой на стиль списка, не оказывает эффекта. Форматирование списка, указанное в самом стиле списка, всегда имеет приоритет.

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

## См. также

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
