---
title: "Aspose::Words::Drawing::ReflectionFormat class"
linktitle: "ReflectionFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ReflectionFormat class. Stellt die Reflexionsformatierung für ein Objekt in C++ dar."
type: docs
weight: 9500
url: /de/cpp/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class


Stellt die Reflexionsformatierung für ein Objekt dar.

```cpp
class ReflectionFormat : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Blur](./get_blur/)() | Ruft einen double-Wert ab oder legt ihn fest, der den Grad des Unschärfeeffekts angibt, der auf den Reflexionseffekt in Punkten angewendet wird. Der Standardwert ist 0.0. |
| [get_Distance](./get_distance/)() | Ruft einen double-Wert ab oder legt ihn fest, der die Menge der Trennung des reflektierten Bildes vom Objekt in Punkten angibt. Der Standardwert ist 0.0. |
| [get_Size](./get_size/)() | Ruft einen double-Wert ab oder legt ihn fest, der die Größe der Reflexion als Prozentsatz des reflektierten Objekts zwischen 0.0 und 1.0 darstellt. Der Standardwert ist 0.0. |
| [get_Transparency](./get_transparency/)() | Ruft einen double-Wert ab oder legt ihn fest, der den Grad der Transparenz für den Reflexionseffekt zwischen 0.0 (undurchsichtig) und 1.0 (klar) darstellt. Der Standardwert ist 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Entfernt [ReflectionFormat](./) aus dem übergeordneten Objekt. |
| [set_Blur](./set_blur/)(double) | Setter für [Aspose::Words::Drawing::ReflectionFormat::get_Blur](./get_blur/). |
| [set_Distance](./set_distance/)(double) | Setter für [Aspose::Words::Drawing::ReflectionFormat::get_Distance](./get_distance/). |
| [set_Size](./set_size/)(double) | Setter für [Aspose::Words::Drawing::ReflectionFormat::get_Size](./get_size/). |
| [set_Transparency](./set_transparency/)(double) | Setter für [Aspose::Words::Drawing::ReflectionFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Hinweise


Verwenden Sie die Eigenschaft [Reflection](../shapebase/get_reflection/), um auf Reflexionseigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der Klasse [ReflectionFormat](./) direkt.

## Beispiele



Zeigt, wie man mit dem Reflexionseffekt einer Form interagiert.
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

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
