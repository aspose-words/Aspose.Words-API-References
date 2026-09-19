---
title: "Aspose::Words::Drawing::ReflectionFormat classe"
linktitle: "ReflectionFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ReflectionFormat classe. Rappresenta la formattazione della riflessione per un oggetto in C++."
type: docs
weight: 9500
url: /it/cpp/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class


Rappresenta la formattazione della riflessione per un oggetto.

```cpp
class ReflectionFormat : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Blur](./get_blur/)() | Ottiene o imposta un valore double che specifica il grado di effetto sfocatura applicato all'effetto di riflessione in punti. Il valore predefinito è 0.0. |
| [get_Distance](./get_distance/)() | Ottiene o imposta un valore double che specifica la quantità di separazione dell'immagine riflessa dall'oggetto in punti. Il valore predefinito è 0.0. |
| [get_Size](./get_size/)() | Ottiene o imposta un valore double compreso tra 0.0 e 1.0 che rappresenta la dimensione della riflessione come percentuale dell'oggetto riflesso. Il valore predefinito è 0.0. |
| [get_Transparency](./get_transparency/)() | Ottiene o imposta un valore double compreso tra 0.0 (opaco) e 1.0 (trasparente) che rappresenta il grado di trasparenza per l'effetto di riflessione. Il valore predefinito è 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Rimuove [ReflectionFormat](./) dall'oggetto padre. |
| [set_Blur](./set_blur/)(double) | Impostatore per [Aspose::Words::Drawing::ReflectionFormat::get_Blur](./get_blur/). |
| [set_Distance](./set_distance/)(double) | Impostatore per [Aspose::Words::Drawing::ReflectionFormat::get_Distance](./get_distance/). |
| [set_Size](./set_size/)(double) | Impostatore per [Aspose::Words::Drawing::ReflectionFormat::get_Size](./get_size/). |
| [set_Transparency](./set_transparency/)(double) | Impostatore per [Aspose::Words::Drawing::ReflectionFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Note


Usa la proprietà [Reflection](../shapebase/get_reflection/) per accedere alle proprietà di riflessione di un oggetto. Non crei istanze della classe [ReflectionFormat](./) direttamente.

## Esempi



Mostra come interagire con l'effetto di forma di riflessione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Reflection()->set_Transparency(0.37);
shape->get_Reflection()->set_Size(0.48);
shape->get_Reflection()->set_Blur(17.5);
shape->get_Reflection()->set_Distance(9.2);

doc->Save(get_ArtifactsDir() + u"Shape.Reflection.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Reflection.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ReflectionFormat> reflectionFormat = shape->get_Reflection();

ASSERT_NEAR(0.37, reflectionFormat->get_Transparency(), 0.01);
ASSERT_NEAR(0.48, reflectionFormat->get_Size(), 0.01);
ASSERT_NEAR(17.5, reflectionFormat->get_Blur(), 0.01);
ASSERT_NEAR(9.2, reflectionFormat->get_Distance(), 0.01);

reflectionFormat->Remove();

ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Transparency());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Size());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Blur());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Distance());
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
