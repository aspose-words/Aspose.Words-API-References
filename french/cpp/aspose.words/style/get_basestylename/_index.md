---
title: "Aspose::Words::Style::get_BaseStyleName méthode"
linktitle: "get_BaseStyleName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Style::get_BaseStyleName méthode. Obtient/definit le nom du style sur lequel ce style est basé en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/style/get_basestylename/
---
## Style::get_BaseStyleName method


Obtient/definit le nom du style sur lequel ce style est basé.

```cpp
System::String Aspose::Words::Style::get_BaseStyleName()
```


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

## Voir aussi

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
