---
title: "Aspose::Words::Drawing::SoftEdgeFormat::get_Radius metod"
linktitle: "get_Radius"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::SoftEdgeFormat::get_Radius metod. Hämtar eller anger ett dubbelvärde som representerar radie‑längden för en mjuk kant‑effekt i punkter (pt). Standardvärdet är 0,0 i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.drawing/softedgeformat/get_radius/
---
## SoftEdgeFormat::get_Radius method


Hämtar eller anger ett dubbelvärde som representerar längden på radien för en mjuk kant-effekt i punkter (pt). Standardvärdet är 0,0.

```cpp
double Aspose::Words::Drawing::SoftEdgeFormat::get_Radius()
```


## Exempel



Visar hur man arbetar med mjuk kantformatering.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Applicera mjuk kant på formen.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Läs in dokument med rektangelform med mjuk kant.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Kontrollera radien för mjuk kant.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Ta bort mjuk kant från formen.
softEdgeFormat->Remove();

// Kontrollera radien för den borttagna mjuka kanten.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```


Visar hur man anger en gräns för bildupplösning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Se även

* Class [SoftEdgeFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
