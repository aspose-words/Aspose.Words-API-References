---
title: "Aspose::Words::Drawing::VerticalAlignment enum"
linktitle: "VerticalAlignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::VerticalAlignment enum. Spécifie l’alignement vertical d’une forme flottante, d’un cadre de texte ou d’une table flottante en C++."
type: docs
weight: 43000
url: /fr/cpp/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enum


Spécifie l’alignement vertical d’une forme flottante, d’un cadre de texte ou d’une table flottante.

```cpp
enum class VerticalAlignment
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | L'objet est positionné explicitement, généralement en utilisant sa propriété **Top**. |
| Top | 1 | Spécifie que l'objet doit être en haut de la base d'alignement vertical. |
| Centre | 2 | Spécifie que l'objet doit être centré par rapport à la base d'alignement vertical. |
| Bottom | 3 | Spécifie que l'objet doit être en bas de la base d'alignement vertical. |
| À l'intérieur | 4 | Spécifie que l'objet doit être à l'intérieur de la base d'alignement horizontal. |
| À l'extérieur | 5 | Spécifie que l'objet doit être à l'extérieur de la base d'alignement vertical. |
| Inline | -1 | Non documenté. Il semble s'agir d'une valeur possible pour les paragraphes et tableaux flottants. |
| Default | n/a | Identique à [None](./). |


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
