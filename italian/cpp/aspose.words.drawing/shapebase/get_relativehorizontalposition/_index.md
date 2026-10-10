---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition metodo"
linktitle: "get_RelativeHorizontalPosition"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition metodo. Specifica rispetto a cosa la shape è posizionata orizzontalmente in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words.drawing/shapebase/get_relativehorizontalposition/
---
## ShapeBase::get_RelativeHorizontalPosition method


Specifica rispetto a cosa la forma è posizionata orizzontalmente.

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition()
```

## Note


Il valore predefinito è [Column](../../relativehorizontalposition/).

Ha effetto solo per le shape flottanti di livello superiore.

## Esempi



Mostra come inserire un'immagine flottante al centro di una pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un'immagine flottante che apparirà dietro il testo sovrapposto e allineala al centro della pagina.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Vedi anche

* Enum [RelativeHorizontalPosition](../../relativehorizontalposition/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
