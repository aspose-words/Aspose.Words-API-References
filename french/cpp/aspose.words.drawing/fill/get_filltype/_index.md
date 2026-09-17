---
title: "Méthode Aspose::Words::Drawing::Fill::get_FillType"
linktitle: "get_FillType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Fill::get_FillType. Obtient un type de remplissage en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.drawing/fill/get_filltype/
---
## Fill::get_FillType method


Obtient le type de remplissage.

```cpp
Aspose::Words::Drawing::FillType Aspose::Words::Drawing::Fill::get_FillType()
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

* Enum [FillType](../../filltype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
