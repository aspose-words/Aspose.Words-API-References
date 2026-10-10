---
title: "Aspose::Words::Style::get_LinkedStyleName méthode"
linktitle: "get_LinkedStyleName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Style::get_LinkedStyleName. Obtient/definit le nom du Style lié à celui-ci. Retourne une chaîne vide si aucun style n’est lié en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words/style/get_linkedstylename/
---
## Style::get_LinkedStyleName method


Obtient/definit le nom du [Style](../) lié à celui-ci. Retourne une chaîne vide si aucun style n’est lié.

```cpp
System::String Aspose::Words::Style::get_LinkedStyleName()
```

## Remarques


Il n’est autorisé de lier le style de paragraphe au style de caractère et vice‑versa.

Définir LinkedStyleName pour le style actuel entraîne automatiquement la définition de LinkedStyleName pour le style lié.

Attribuer une chaîne vide équivaut à dissocier le style précédemment lié.

## Exemples



Montre comment utiliser les alias de style.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// Ce document contient un style nommé "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Si le nom d'un style comporte plusieurs valeurs séparées par des virgules, chaque clause est un alias distinct.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// Nous pouvons référencer un style en utilisant son alias, ainsi que son nom.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```


Montre comment lier les styles entre eux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);

System::SharedPtr<Aspose::Words::Style> styleHeading1Char = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"Heading 1 Char");
styleHeading1Char->get_Font()->set_Name(u"Verdana");
styleHeading1Char->get_Font()->set_Bold(true);
styleHeading1Char->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::Dot);
styleHeading1Char->get_Font()->get_Border()->set_LineWidth(15);

styleHeading1->set_LinkedStyleName(u"Heading 1 Char");

ASSERT_EQ(u"Heading 1 Char", styleHeading1->get_LinkedStyleName());
ASSERT_EQ(u"Heading 1", styleHeading1Char->get_LinkedStyleName());
```

## Voir aussi

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
