---
title: "Aspose::Words::Drawing::GradientStopCollection::RemoveAt metodo"
linktitle: "RemoveAt"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::GradientStopCollection::RemoveAt metodo. Rimuove un GradientStop dalla collezione a un indice specificato in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.drawing/gradientstopcollection/removeat/
---
## GradientStopCollection::RemoveAt method


Rimuove un [GradientStop](../../gradientstop/) dalla collezione a un indice specificato.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GradientStop> Aspose::Words::Drawing::GradientStopCollection::RemoveAt(int32_t index)
```


### ReturnValue

Rimosso [GradientStop](../../gradientstop/).

## Esempi



Mostra come aggiungere gradient stop al riempimento del gradiente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
shape->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Green(), System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2);

// Ottieni la collezione di gradient stop.
System::SharedPtr<Aspose::Words::Drawing::GradientStopCollection> gradientStops = shape->get_Fill()->get_GradientStops();

// Modifica il primo gradient stop.
gradientStops->idx_get(0)->set_Color(System::Drawing::Color::get_Aqua());
gradientStops->idx_get(0)->set_Position(0.1);
gradientStops->idx_get(0)->set_Transparency(0.25);

// Aggiungi un nuovo gradient stop alla fine della collezione.
auto gradientStop = System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Brown(), 0.5);
gradientStops->Add(gradientStop);

// Rimuovi il gradient stop all'indice 1.
gradientStops->RemoveAt(1);
// E inserisci un nuovo gradient stop allo stesso indice 1.
gradientStops->Insert(1, System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Chocolate(), 0.75, 0.3));

// Rimuovi l'ultimo gradient stop nella collezione.
gradientStop = gradientStops->idx_get(2);
gradientStops->Remove(gradientStop);

ASSERT_EQ(2, gradientStops->get_Count());

ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 0, 255, 255), gradientStops->idx_get(0)->get_BaseColor());
ASSERT_EQ(System::Drawing::Color::get_Aqua().ToArgb(), gradientStops->idx_get(0)->get_Color().ToArgb());
ASSERT_NEAR(0.1, gradientStops->idx_get(0)->get_Position(), 0.01);
ASSERT_NEAR(0.25, gradientStops->idx_get(0)->get_Transparency(), 0.01);

ASSERT_EQ(System::Drawing::Color::get_Chocolate().ToArgb(), gradientStops->idx_get(1)->get_Color().ToArgb());
ASSERT_NEAR(0.75, gradientStops->idx_get(1)->get_Position(), 0.01);
ASSERT_NEAR(0.3, gradientStops->idx_get(1)->get_Transparency(), 0.01);

// Usa l'opzione di conformità per definire la forma usando DML
// se vuoi ottenere la proprietà "GradientStops" dopo che il documento è stato salvato.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientStops.docx", saveOptions);
```

## Vedi anche

* Class [GradientStop](../../gradientstop/)
* Class [GradientStopCollection](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
