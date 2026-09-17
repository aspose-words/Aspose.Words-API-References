---
title: "Aspose::Words::Drawing::Stroke::get_ImageBytes méthode"
linktitle: "get_ImageBytes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Stroke::get_ImageBytes méthode. Définit l'image pour un remplissage d'image ou de motif de trait en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.drawing/stroke/get_imagebytes/
---
## Stroke::get_ImageBytes method


Définit l'image pour un remplissage d'image ou de motif de trait.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::Stroke::get_ImageBytes()
```


## Exemples



Montre comment traiter les caractéristiques du trait de forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();

// Les traits peuvent avoir deux couleurs, qui sont utilisées pour créer un motif défini par des données d'image bicolores.
// Les traits avec une seule couleur n'utilisent pas la propriété Color2.
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(System::TestTools::IsNull(stroke->get_ImageBytes()));
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## Voir aussi

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
