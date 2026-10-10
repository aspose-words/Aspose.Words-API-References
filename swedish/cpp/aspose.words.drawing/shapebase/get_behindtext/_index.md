---
title: "Aspose::Words::Drawing::ShapeBase::get_BehindText metod"
linktitle: "get_BehindText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_BehindText metod. Anger om formen är under eller över text i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.drawing/shapebase/get_behindtext/
---
## ShapeBase::get_BehindText method


Anger om formen är under eller över text.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_BehindText()
```

## Anmärkningar


Har endast effekt för former på toppnivå.

Standardvärdet är **false**.

## Exempel



Visar hur man infogar en flytande bild i sidans centrum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en flytande bild som visas bakom den överlappande texten och justera den till sidans centrum.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
