---
title: "Aspose::Words::Drawing::ShapeBase::get_BehindText Methode"
linktitle: "get_BehindText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_BehindText Methode. Gibt an, ob die Form unter oder über dem Text liegt in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.drawing/shapebase/get_behindtext/
---
## ShapeBase::get_BehindText method


Gibt an, ob die Form unter oder über dem Text liegt.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_BehindText()
```

## Hinweise


Wirkt nur bei Formen der obersten Ebene.

Der Standardwert ist **false**.

## Beispiele



Zeigt, wie man ein schwebendes Bild in die Mitte einer Seite einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text erscheint und es an der Seitenmitte ausrichtet.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
