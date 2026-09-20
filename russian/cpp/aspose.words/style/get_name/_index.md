---
title: "Aspose::Words::Style::get_Name метод"
linktitle: "get_Name"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Style::get_Name метод. Получает или задает имя стиля в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words/style/get_name/
---
## Style::get_Name method


Получает или устанавливает имя стиля.

```cpp
System::String Aspose::Words::Style::get_Name() const
```

## Примечания


Не может быть пустой строкой.

Если в коллекции уже существует стиль с таким именем, то этот стиль заменит его. Все затронутые узлы будут ссылаться на новый стиль.

## Примеры



Показывает, как получить доступ к коллекции стилей документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Перечислите и выведите список всех стилей, которые документ, созданный с помощью Aspose.Words, содержит по умолчанию.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> stylesEnum = doc->get_Styles()->GetEnumerator();
    while (stylesEnum->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Style> curStyle = stylesEnum->get_Current();
        std::cout << System::String::Format(u"Style name:\t\"{0}\", of type \"{1}\"", curStyle->get_Name(), curStyle->get_Type()) << std::endl;
        std::cout << System::String::Format(u"\tSubsequent style:\t{0}", curStyle->get_NextParagraphStyleName()) << std::endl;
        std::cout << System::String::Format(u"\tIs heading:\t\t\t{0}", curStyle->get_IsHeading()) << std::endl;
        std::cout << System::String::Format(u"\tIs QuickStyle:\t\t{0}", curStyle->get_IsQuickStyle()) << std::endl;

        ASPOSE_ASSERT_EQ(doc, curStyle->get_Document());
    }
}
```


Показывает, как клонировать стиль документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Метод AddCopy создает копию указанного стиля и
// автоматически генерирует новое имя для стиля, например "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Используйте свойство "Name" стиля, чтобы изменить идентифицирующее имя стиля.
newStyle->set_Name(u"My Heading 1");

// В нашем документе теперь есть два визуально одинаковых стиля с разными именами.
// Изменение настроек одного из стилей не влияет на другой.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```

## См. также

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
