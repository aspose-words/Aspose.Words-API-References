---
title: "Aspose::Words::Drawing::GradientStopCollection classe"
linktitle: "GradientStopCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::GradientStopCollection classe. Contiene una collezione di oggetti GradientStop. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class


Contiene una collezione di oggetti [GradientStop](../gradientstop/). Per saperne di più, visita l'articolo di documentazione [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class GradientStopCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::GradientStop>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Aggiunge un [GradientStop](../gradientstop/) specificato a un gradiente. |
| [get_Count](./get_count/)() | Restituisce un valore intero che indica il numero di elementi nella collezione. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un enumeratore che itera attraverso la raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta un oggetto [GradientStop](../gradientstop/) nella collezione. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Ottiene o imposta un oggetto [GradientStop](../gradientstop/) nella collezione. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Inserisce un [GradientStop](../gradientstop/) nella collezione a un indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Rimuove un [GradientStop](../gradientstop/) specificato dalla collezione. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un [GradientStop](../gradientstop/) dalla collezione a un indice specificato. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
