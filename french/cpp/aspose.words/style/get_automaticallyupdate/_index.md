---
title: "Méthode Aspose::Words::Style::get_AutomaticallyUpdate"
linktitle: "get_AutomaticallyUpdate"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Style::get_AutomaticallyUpdate. Indique si ce style est automatiquement redéfini en fonction de la valeur appropriée en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/style/get_automaticallyupdate/
---
## Style::get_AutomaticallyUpdate method


Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée.

```cpp
bool Aspose::Words::Style::get_AutomaticallyUpdate() const
```

## Remarques


Si la valeur de la propriété est définie sur true, MS Word redéfinit automatiquement le style actuel lorsque le formatage du paragraphe approprié a été modifié.

La propriété AutomaticallyUpdate ne s'applique qu'aux styles de paragraphe.

La valeur par défaut est **false**.

## Exemples



Montre comment créer et appliquer un style personnalisé.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Redéfinir automatiquement le style.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Applique l'un des styles du document au paragraphe que le constructeur de document est en train de créer.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Supprime notre style personnalisé de la collection de styles du document.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Tout texte qui utilisait un style supprimé revient au formatage par défaut.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```

## Voir aussi

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
