---
title: "Méthode Aspose::Words::Font::get_Style"
linktitle: "get_Style"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_Style. Obtient ou définit le style de caractère appliqué à ce formatage en C++."
type: docs
weight: 42000
url: /fr/cpp/aspose.words/font/get_style/
---
## Font::get_Style method


Obtient ou définit le style de caractère appliqué à ce formatage.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Font::get_Style()
```


## Exemples



Applique un double soulignement à toutes les séquences d'un document qui sont formatées avec des styles de caractères personnalisés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un style personnalisé et appliquez-le au texte créé à l'aide d'un constructeur de document.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Red());
style->get_Font()->set_Name(u"Courier New");

builder->get_Font()->set_StyleName(u"MyStyle");
builder->Write(u"This text is in a custom style.");

// Itérez sur chaque séquence et ajoutez un double soulignement à chaque style personnalisé.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    System::SharedPtr<Aspose::Words::Style> charStyle = run->get_Font()->get_Style();

    if (!charStyle->get_BuiltIn())
    {
        run->get_Font()->set_Underline(Aspose::Words::Underline::Double);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.Style.docx");
```

## Voir aussi

* Class [Style](../../style/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
