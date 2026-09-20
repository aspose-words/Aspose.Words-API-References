---
title: "Aspose::Words::Lists::List::get_Style метод"
linktitle: "get_Style"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::List::get_Style метод. Получает стиль списка, на который ссылается данный список, или определяет его в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.lists/list/get_style/
---
## List::get_Style method


Получает стиль списка, на который этот список ссылается или который определяет.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Lists::List::get_Style()
```

## Примечания


Если этот список не связан со стилем списка, свойство вернёт **null**.

Список может быть ссылкой на стиль списка, в этом случае [IsListStyleReference](../get_isliststylereference/) будет **true**.

Список может быть определением стиля списка, в этом случае [IsListStyleDefinition](../get_isliststyledefinition/) будет **true**. Такой список нельзя применять напрямую к абзацам в документе.

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

* Class [Style](../../../aspose.words/style/)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
