---
title: "Aspose::Words::Drawing::ShadowFormat::get_Color méthode"
linktitle: "get_Color"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShadowFormat::get_Color méthode. Obtient ou définit un objet Color qui représente la couleur de l'ombre. La valeur par défaut est Black en C++."
type: docs
weight: 2500
url: /fr/cpp/aspose.words.drawing/shadowformat/get_color/
---
## ShadowFormat::get_Color method


Obtient ou définit un objet **Color** qui représente la couleur de l'ombre. La valeur par défaut est **Black**.

```cpp
System::Drawing::Color Aspose::Words::Drawing::ShadowFormat::get_Color()
```


## Exemples



Montre comment obtenir la couleur de l'ombre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```


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
