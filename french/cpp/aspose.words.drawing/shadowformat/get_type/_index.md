---
title: "Aspose::Words::Drawing::ShadowFormat::get_Type méthode"
linktitle: "get_Type"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShadowFormat::get_Type méthode. Obtient ou définit le ShadowType spécifié pour ShadowFormat en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.drawing/shadowformat/get_type/
---
## ShadowFormat::get_Type method


Obtient ou définit le [ShadowType](../../shadowtype/) spécifié pour [ShadowFormat](../).

```cpp
Aspose::Words::Drawing::ShadowType Aspose::Words::Drawing::ShadowFormat::get_Type()
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

## Voir aussi

* Enum [ShadowType](../../shadowtype/)
* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
