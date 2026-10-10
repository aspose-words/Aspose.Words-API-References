---
title: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage Methode"
linktitle: "get_CanHaveImage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage Methode. Gibt **true** zurück, wenn der Formtyp es erlaubt, dass die Form ein Bild in C++ hat."
type: docs
weight: 12000
url: /de/cpp/aspose.words.drawing/shapebase/get_canhaveimage/
---
## ShapeBase::get_CanHaveImage method


Gibt **true** zurück, wenn der Formtyp es erlaubt, dass die Form ein Bild hat.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_CanHaveImage()
```

## Hinweise


Obwohl Microsoft Word einen speziellen Formtyp für Bilder hat, scheint es, dass in Microsoft Word-Dokumenten jede Form außer einer Gruppierungsform ein Bild haben kann, daher gibt diese Eigenschaft **true** für alle Formen außer [GroupShape](../../groupshape/) zurück.

## Beispiele



Zeigt, wie man ein Bild einfügt und rotiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Füge eine Form mit einem Bild ein.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Rotiere das Bild um 45 Grad im Uhrzeigersinn.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
