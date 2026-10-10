---
title: "Méthode Aspose::Words::Style::get_Name"
linktitle: "get_Name"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Style::get_Name. Obtient ou définit le nom du style en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words/style/get_name/
---
## Style::get_Name method


Obtient ou définit le nom du style.

```cpp
System::String Aspose::Words::Style::get_Name() const
```

## Remarques


Ne peut pas être une chaîne vide.

S'il existe déjà un style portant ce nom dans la collection, alors ce style le remplacera. Tous les nœuds affectés référenceront le nouveau style.

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


Montre comment cloner le style d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// La méthode AddCopy crée une copie du style spécifié et
// génère automatiquement un nouveau nom pour le style, tel que "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Utilisez la propriété "Name" du style pour modifier le nom d'identification du style.
newStyle->set_Name(u"My Heading 1");

// Notre document possède maintenant deux styles identiques en apparence avec des noms différents.
// Modifier les paramètres de l'un des styles n'affecte pas l'autre.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```

## Voir aussi

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
