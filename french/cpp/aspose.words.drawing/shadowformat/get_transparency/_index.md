---
title: "Aspose::Words::Drawing::ShadowFormat::get_Transparency méthode"
linktitle: "get_Transparency"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShadowFormat::get_Transparency méthode. Obtient ou définit le degré de transparence de l'effet d'ombre sous forme d'une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). La valeur par défaut est 0.0 en C++."
type: docs
weight: 2750
url: /fr/cpp/aspose.words.drawing/shadowformat/get_transparency/
---
## ShadowFormat::get_Transparency method


Obtient ou définit le degré de transparence de l'effet d'ombre comme une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). La valeur par défaut est 0.0.

```cpp
double Aspose::Words::Drawing::ShadowFormat::get_Transparency()
```


## Exemples



Montre comment définir une couleur avec transparence.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();
shadowFormat->set_Type(Aspose::Words::Drawing::ShadowType::Shadow21);
shadowFormat->set_Color(System::Drawing::Color::get_Red());
shadowFormat->set_Transparency(0.8);

doc->Save(get_ArtifactsDir() + u"Shape.ShadowFormatTransparency.docx");
```

## Voir aussi

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
