---
title: "Aspose::Words::Font::get_Fill méthode"
linktitle: "get_Fill"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_Fill méthode. Obtient le format de remplissage pour la Font en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words/font/get_fill/
---
## Font::get_Fill method


Obtient le format de remplissage pour la [Font](../).

```cpp
System::SharedPtr<Aspose::Words::Drawing::Fill> Aspose::Words::Font::get_Fill()
```


## Exemples



Montre comment convertir n'importe quel remplissage en remplissage plein.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Two color gradient.docx");

// Obtenir l'objet Fill pour la police du premier Run.
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// Vérifier les propriétés Fill de la police.
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// Changer le type du remplissage en plein avec une couleur verte uniforme.
fill->Solid();
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## Voir aussi

* Class [Fill](../../../aspose.words.drawing/fill/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
