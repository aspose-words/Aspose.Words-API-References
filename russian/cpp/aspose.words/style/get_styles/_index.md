---
title: "Aspose::Words::Style::get_Styles метод"
linktitle: "get_Styles"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Style::get_Styles метод. Получает коллекцию стилей, к которым принадлежит данный стиль в C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words/style/get_styles/
---
## Style::get_Styles method


Получает коллекцию стилей, к которым принадлежит этот стиль.

```cpp
System::SharedPtr<Aspose::Words::StyleCollection> Aspose::Words::Style::get_Styles() const
```


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

## См. также

* Class [StyleCollection](../../stylecollection/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
