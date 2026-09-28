---
title: "Aspose::Words::DocumentBase::get_Styles метод"
linktitle: "get_Styles"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBase::get_Styles метод. Возвращает коллекцию стилей, определённых в документе, на C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/documentbase/get_styles/
---
## DocumentBase::get_Styles method


Возвращает коллекцию стилей, определённых в документе.

```cpp
System::SharedPtr<Aspose::Words::StyleCollection> Aspose::Words::DocumentBase::get_Styles() const
```

## Примечания


Для получения дополнительной информации см. описание класса [StyleCollection](../../stylecollection/) .

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


Показывает, как создать и использовать абзацный стиль со списковой разметкой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте пользовательский абзацный стиль.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Примените абзацный стиль к текущему абзацу DocumentBuilder, а затем добавьте некоторый текст.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Измените стиль DocumentBuilder на такой, который не содержит форматирования списка, и напишите еще один абзац.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## См. также

* Class [StyleCollection](../../stylecollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
