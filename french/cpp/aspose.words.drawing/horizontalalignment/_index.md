---
title: "Aspose::Words::Drawing::HorizontalAlignment énumération"
linktitle: "HorizontalAlignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::HorizontalAlignment énumération. Spécifie l'alignement horizontal d'une forme flottante, d'un cadre de texte ou d'un tableau flottant en C++."
type: docs
weight: 26000
url: /fr/cpp/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enum


Spécifie l'alignement horizontal d'une forme flottante, d'un cadre de texte ou d'un tableau flottant.

```cpp
enum class HorizontalAlignment
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | L'objet est positionné explicitement, généralement en utilisant sa propriété **Left**. |
| Default | n/a | Identique à [None](./). |
| Gauche | 1 | Spécifie que l'objet doit être aligné à gauche par rapport à la base d'alignement horizontal. |
| Centre | 2 | Spécifie que l'objet doit être centré par rapport à la base d'alignement horizontal. |
| Droite | 3 | Spécifie que l'objet doit être aligné à droite par rapport à la base d'alignement horizontal. |
| À l'intérieur | 4 | Spécifie que l'objet doit être à l'intérieur de la base d'alignement horizontal. |
| À l'extérieur | 5 | Spécifie que l'objet doit être à l'extérieur de la base d'alignement horizontal. |


## Exemples



Montre comment insérer une image flottante au centre d'une page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une image flottante qui apparaîtra derrière le texte qui se chevauche et alignez‑la au centre de la page.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
