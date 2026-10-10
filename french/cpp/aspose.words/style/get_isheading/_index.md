---
title: "Aspose::Words::Style::get_IsHeading méthode"
linktitle: "get_IsHeading"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Style::get_IsHeading méthode. Vrai lorsque le style fait partie des styles Titre intégrés en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/style/get_isheading/
---
## Style::get_IsHeading method


Vrai lorsque le style fait partie des styles de titre intégrés.

```cpp
bool Aspose::Words::Style::get_IsHeading()
```


## Exemples



Montre comment accéder à la collection de styles d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Énumère et répertorie tous les styles qu'un document créé avec Aspose.Words contient par défaut.
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

## Voir aussi

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
